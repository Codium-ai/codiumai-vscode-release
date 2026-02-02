//@version=5

indicator(title='Purra Buy Sell-indicator.lk', shorttitle='Purra Buy Sell Signals', overlay=true)

// PMI_LA Indicator Parameters
sm = input(6, title='PMI_LA Smoothing Period')
cd = input(0.4, title='PMI_LA Constant D')
ebc = input(false, title='PMI_LA Color Bars')
ribm = input(false, title='PMI_LA Ribbon Mode')

// Buy Sell Indicator Parameters
a = input(2, title='BSI Multiplier')
c = input(30, title='BSI ATR Period')
h = input(false, title='BSI Heikin Ashi Candles')

// PMI_LA Calculation
var float i1 = na
var float i2 = na
var float i3 = na
var float i4 = na
var float i5 = na
var float i6 = na
var float bfr = na
var color bfrC = na
var float di = na
var float c1 = na
var float c2 = na
var float c3 = na
var float c4 = na
var float c5 = na

src_pmi = close
di := (sm - 1.0) / 2.0 + 1.0
c1 := 2 / (di + 1.0)
c2 := 1 - c1
c3 := 3.0 * (cd * cd + cd * cd * cd)
c4 := -3.0 * (2.0 * cd * cd + cd + cd * cd * cd)
c5 := 3.0 * cd + 1.0 + cd * cd * cd + 3.0 * cd * cd
i1 := c1 * src_pmi + c2 * nz(i1[1])
i2 := c1 * i1 + c2 * nz(i2[1])
i3 := c1 * i2 + c2 * nz(i3[1])
i4 := c1 * i3 + c2 * nz(i4[1])
i5 := c1 * i4 + c2 * nz(i5[1])
i6 := c1 * i5 + c2 * nz(i6[1])
bfr := -cd * cd * cd * i6 + c3 * i5 + c4 * i4 + c5 * i3
bfrC := bfr > nz(bfr[1]) ? color.green : bfr < nz(bfr[1]) ? color.red : color.blue

// Buy Sell Indicator Calculation
xATR = ta.atr(c)
nLoss = a * xATR
src_bsi = h ? request.security(ticker.heikinashi(syminfo.tickerid), timeframe.period, close, lookahead=barmerge.lookahead_off) : close
var float xATRTrailingStop = na
iff_1 = src_bsi > nz(xATRTrailingStop[1], 0) ? src_bsi - nLoss : src_bsi + nLoss
iff_2 = src_bsi < nz(xATRTrailingStop[1], 0) and src_bsi[1] < nz(xATRTrailingStop[1], 0) ? math.min(nz(xATRTrailingStop[1]), src_bsi + nLoss) : iff_1
xATRTrailingStop := src_bsi > nz(xATRTrailingStop[1], 0) and src_bsi[1] > nz(xATRTrailingStop[1], 0) ? math.max(nz(xATRTrailingStop[1]), src_bsi - nLoss) : iff_2
var int pos = na
pos := src_bsi[1] < nz(xATRTrailingStop[1], 0) and src_bsi > nz(xATRTrailingStop[1], 0) ? 1 : src_bsi[1] > nz(xATRTrailingStop[1], 0) and src_bsi < nz(xATRTrailingStop[1], 0) ? -1 : nz(pos[1], 0)

xcolor = pos == -1 ? color.red : pos == 1 ? color.green : color.blue
ema = ta.ema(src_bsi, 1)
above = ta.crossover(ema, xATRTrailingStop)
below = ta.crossover(xATRTrailingStop, ema)
buy = src_bsi > xATRTrailingStop and above
sell = src_bsi < xATRTrailingStop and below

// Plotting
plot(ribm ? na : bfr, title='PMI_LA Trend', linewidth=3, color=bfrC)
bgcolor(ribm ? bfrC : na, transp=50)
// This work is licensed under a Attribution-NonCommercial-ShareAlike 4.0 International (CC BY-NC-SA 4.0) https://creativecommons.org/licenses/by-nc-sa/4.0/
// Inspired by LuxAlgo Nadaraya-Watson Envelope
//@version=5

indicator("Nadaraya-Watson Envelope: Modified by Yosiet",overlay=true,max_bars_back=1000,max_lines_count=500,max_labels_count=500)
length = input.float(500,'Window Size',maxval=500,minval=0)
h      = input.float(10.,'Bandwidth')
mult   = input.float(3.) 
srcUpperBand = input.source(low,'Source Upper Band')
src    = input.source(high,'Source Lower Band')


up_col = input.color(#ff1100,'Colors',inline='col')
dn_col = input.color(#39ff14,'',inline='col')
show_bands = input(false, 'Show Bands')
show_sma_7_low_1 = input(false, 'Show SMA 7 LOW +1')
show_sma_7_low_7 = input(false, 'Show SMA 7 LOW -7')
show_sma_30_high = input(false, 'Show SMA 30 HIGH')
//----
n = bar_index
var k = 2
var upper = array.new_line(0) 
var lower = array.new_line(0) 

sma7_low = ta.sma(low, 7)
sma30_high = ta.sma(high, 30)

strDownArrows = "▼"
strUpArrows = "▲"

RoundUp(number, decimals) =>
    factor = math.pow(10, decimals)
    math.ceil(number * factor) / factor

plot(show_sma_7_low_1?sma7_low:na, color=color.rgb(255, 235, 59, 81), title="SMA 7 LOW +1", offset=+1, linewidth=1)
plot(show_sma_7_low_7?sma7_low:na, color=color.rgb(255, 235, 59, 81), title="7 sma", offset=-7, linewidth=1)
plot(show_sma_30_high ? sma30_high:na, color=color.purple, title="SMA 30 High", linewidth=1)
lset(l,x1,y1,x2,y2,col)=>
    line.set_xy1(l,x1,y1)
    line.set_xy2(l,x2,y2)
    line.set_color(l,col)
    line.set_width(l,2)

if barstate.isfirst
    for i = 0 to length/k-1
        array.push(upper,line.new(na,na,na,na))
        array.push(lower,line.new(na,na,na,na))
//----
line up = na
line dn = na
//----
cross_up = 0.
cross_dn = 0.
if barstate.islast
    y = array.new_float(0)
    yUpper = array.new_float(0)
    
    sum_upper_e = 0.
    sum_e = 0.
    for i = 0 to length-1
        sum_upper = 0.
        sumw_upper = 0.
        sum = 0.
        sumw = 0.
        
        for j = 0 to length-1
            w = math.exp(-(math.pow(i-j,2)/(h*h*2)))
            sum_upper += srcUpperBand[j]*w
            sum += src[j]*w
            sumw += w
        
        y_upper_2 = sum_upper/sumw
        sum_upper_e += math.abs(srcUpperBand[i] - y_upper_2)
        array.push(yUpper,y_upper_2)

        y2 = sum/sumw
        sum_e += math.abs(src[i] - y2)
        array.push(y,y2)

    mae_upper = sum_upper_e/length*mult
    mae = sum_e/length*mult
    
    for i = 1 to length-1
        upper_y2 = array.get(yUpper,i)
        upper_y1 = array.get(yUpper,i-1)

        y2 = array.get(y,i)
        y1 = array.get(y,i-1)
        
        up := array.get(upper,i/k) 
        dn := array.get(lower,i/k)

        //draw borders bands
        if show_bands
            lset(up,n-i+1,upper_y1 + mae_upper,n-i,upper_y2 + mae_upper,up_col)
            lset(dn,n-i+1,y1 - mae,n-i,y2 - mae,dn_col)
        
        //draw fractals
        //if src[i] > y1 + mae and src[i+1] < y1 + mae
        //    label.new(n-i,src[i],strDownArrows,color=#00000000,style=label.style_label_down,textcolor=dn_col,textalign=text.align_center)
        //if src[i] < y1 - mae and src[i+1] > y1 - mae
        //    label.new(n-i,src[i],strUpArrows,color=#00000000,style=label.style_label_up,textcolor=up_col,textalign=text.align_center)
        
        //draw sma 30 high signals
        if sma30_high[i] > upper_y1 + mae_upper and sma30_high[i+1] < upper_y2 + mae_upper
            label.new(n-i,srcUpperBand[i]+mae_upper,strDownArrows,color=#00000000,style=label.style_label_down,textcolor=#ec05af,textalign=text.align_center)
        //if sma30_high[i] < y1 - mae and sma30_high[i+1] > y2 - mae
        //    label.new(n-i,src[i+1],strUpArrows,color=#00000000,style=label.style_label_down,textcolor=#ec05af,textalign=text.align_center)

        //draw sma 7 low signals
        if sma7_low[i] > upper_y1 + mae_upper and sma7_low[i+1] < upper_y2 + mae_upper
            label.new(n-i,src[i],strDownArrows,color=#00000000,style=label.style_label_down,textcolor=color.orange,textalign=text.align_center)
        if sma7_low[i] < y1 - mae and sma7_low[i+1] > y2 - mae
            label.new(n-i,src[i]-mae,strUpArrows,color=#00000000,style=label.style_label_up,textcolor=color.orange,textalign=text.align_center)
		
    cross_up := array.get(yUpper,0) + mae_upper
    cross_dn := array.get(y,0) - mae	

sma7_crossover = ta.crossover(sma7_low,cross_up)
sma7_crossunder = ta.crossunder(sma7_low,cross_dn)

sma30_crossover = ta.crossover(sma30_high,cross_up)
sma30_crossunder = ta.crossunder(sma30_high,cross_dn)

alertcondition(sma30_crossunder or sma7_crossunder,title="LONG", message='LONG: {{ticker}}/{{interval}} at price {{close}} on {{exchange}}' )
alertcondition(sma7_crossover or sma30_crossover,title="SHORT", message='SHORT: {{ticker}}/{{interval}} at price {{close}} on {{exchange}}' )
plotshape(buy, title='Buy', text='Buy', style=shape.labelup, location=location.belowbar, color=color.new(color.green, 0), textcolor=color.new(color.black, 0), size=size.tiny)
plotshape(sell, title='Sell', text='Sell', style=shape.labeldown, location=location.abovebar, color=color.new(color.red, 0), textcolor=color.new(color.black, 0), size=size.tiny)

barcolor(buy ? color.green : sell ? color.red : na)

alertcondition(buy, 'Purra Long', 'Purra Long')
alertcondition(sell, 'Purra Short', 'Purra Short')
// This source code is subject to the terms of the Mozilla Public License 2.0 at https://mozilla.org/MPL/2.0/
// © nicks1008
//@version=4
study("SWING CALLS",title="SMA call buy/sale",shorttitle = "SWING CALL",precision=1, overlay=true)
ema_value=input(5)
sma_value=input(50)
ema1=ema(close,ema_value)
sma2= sma(close,sma_value)
rs=rsi(close,14)

mycolor= iff(rs>=85 or rs<=15,color.yellow,iff(low> sma2,color.lime,iff(high<sma2,color.red,color.yellow)))

hl=input(80,title="Overbought limit of RSI",step=1)
ll=input(20,title="Oversold limit of RSI",step=1)


buyexit= crossunder(rs,hl)
sellexit=crossover(rs,ll)


plot(sma2,title="Long SMA",color=mycolor,linewidth=2,transp=40)

plotshape(buyexit,title="RSI alert Bearish", style=shape.triangledown,
                 location=location.abovebar, color=color.teal, text="↓\n ↓")
plotshape(sellexit,title="RSI alert Bullish", style=shape.triangleup,
                 location=location.belowbar, color=color.teal, text="↑ \n ↑")    
                 
sellcall= crossover(sma2,ema1)and open>close
buycall=crossunder (sma2,ema1)and high>sma2
                 
plotshape(buycall,title="BuyShape", style=shape.labelup,
                   location=location.belowbar, color=color.aqua, text="B",textcolor=color.white)
plotshape(sellcall,title="SellShape", style=shape.labeldown,
                   location=location.abovebar, color=color.red,transp=20, text="S",textcolor=color.black) 
                   
alertcondition(buyexit or sellexit,title="Reversal", message="Possible Reversal on Swing Signal Alert") 
alertcondition(buycall or sellcall,title="Buy/Sale Swing Signal", message="Swing Signal Entry Alert") 
// This Pine Script™ code is subject to the terms of the Mozilla Public License 2.0 at https://mozilla.org/MPL/2.0/
// © QuantAlgo

//@version=6
indicator(title="Zero Lag Signals For Loop [QuantAlgo]", overlay=true)

//              ╔════════════════════════════════╗              //
//              ║      USER-DEFINED SETTINGS     ║              //
//              ╚════════════════════════════════╝              //

// Input Groups
var string zlag_settings    = "════════ Zero Lag Settings ════════"
var string loop_settings    = "════════ For Loop Settings ════════"
var string thresh_settings  = "════════ Threshold Settings ════════"
var string visual_settings  = "════════ Visualization Settings ════════"

// Tooltips
tooltip_zl_length     = "Length of the Zero Lag calculation period. Higher values create smoother signals."
tooltip_vol_mult      = "Multiplier for volatility in signal generation. Higher values make signals more conservative by requiring larger price movements."
tooltip_loop_start    = "Starting point for the loop analysis. Lower values analyze more recent price action."
tooltip_loop_end      = "Ending point for the loop analysis. Higher values analyze longer historical periods."
tooltip_thresh_up     = "Minimum score required to generate uptrend signals. Higher values create stricter conditions."
tooltip_thresh_down   = "Maximum score required to generate downtrend signals. Lower values create stricter conditions."
tooltip_signals       = "Enable/disable signal markers on the chart"
tooltip_candles       = "Enable/disable candle coloring based on trend direction"
tooltip_bg_lines      = "Enable/disable vertical lines on signal changes"

// Zero Lag Settings
length = input.int(50, "Zero Lag Length", 
     minval=1, 
     group=zlag_settings, 
     tooltip=tooltip_zl_length)
volatility_mult = input.float(1.5, "Volatility Multiplier", 
     minval=0.1, 
     group=zlag_settings, 
     tooltip=tooltip_vol_mult)

// Loop Settings
loop_start = input.int(1, "Loop Start", 
     minval=1, 
     group=loop_settings, 
     tooltip=tooltip_loop_start)
loop_end = input.int(70, "Loop End", 
     minval=1, 
     group=loop_settings, 
     tooltip=tooltip_loop_end)

// Threshold Settings
threshold_up = input.int(5, "Threshold Uptrend", 
     group=thresh_settings, 
     tooltip=tooltip_thresh_up)
threshold_down = input.int(-5, "Threshold Downtrend", 
     group=thresh_settings, 
     tooltip=tooltip_thresh_down)

// Visualization Settings
bullcolor = input.color(#00ffaa, "Bullish Color", group=visual_settings)
bearcolor = input.color(#ff0000, "Bearish Color", group=visual_settings)
show_signals = input.bool(true, "Show Signal Markers", 
     group=visual_settings, tooltip=tooltip_signals)
paint_candles = input.bool(true, "Color Candles", 
     group=visual_settings, tooltip=tooltip_candles)
show_bg_lines = input.bool(false, "Signal Change Lines", 
     group=visual_settings, tooltip=tooltip_bg_lines)

//              ╔════════════════════════════════╗              //
//              ║      ZERO LAG CALCULATIONS     ║              //
//              ╚════════════════════════════════╝              //

lag = math.floor((length - 1) / 2)
zl_basis = ta.ema(close + (close - close[lag]), length)
volatility = ta.highest(ta.atr(length), length*3) * volatility_mult

//              ╔════════════════════════════════╗              //
//              ║        FOR LOOP ANALYSIS       ║              //
//              ╚════════════════════════════════╝              //

forloop_analysis(basis_price) =>
    sum = 0.0
    for i = loop_start to loop_end by 1
        sum += (basis_price > basis_price[i] ? 1 : -1)
    sum

score = forloop_analysis(zl_basis)

//              ╔════════════════════════════════╗              //
//              ║        SIGNAL GENERATION       ║              //
//              ╚════════════════════════════════╝              //

// Long/Short conditions
long_signal = score > threshold_up and close > zl_basis + volatility
short_signal = score < threshold_down and close < zl_basis - volatility

// Trend detection
var trend = 0
if long_signal
    trend := 1
else if short_signal
    trend := -1

// Track trend changes
var prev_trend = 0
trend_changed = trend != prev_trend
prev_trend := trend

//              ╔════════════════════════════════╗              //
//              ║         VISUALIZATION          ║              //
//              ╚════════════════════════════════╝              //

// Current trend color
trend_col = trend == 1 ? bullcolor : trend == -1 ? bearcolor : na

// Plot Zero Lag line
p_basis = plot(zl_basis, "Zero Lag Basis", color=trend_col, linewidth=3)
p_price = plot(hl2, "Price", display=display.none, editable=false)

// Fill between Zero Lag and price
fill(p_basis, p_price, hl2, zl_basis, na, color.new(trend_col, 20))

// Plot trend shift labels
plotshape(trend_changed and trend == 1 ? zl_basis : na, "Bullish Trend", 
     shape.labelup, location.absolute, bullcolor, 
     text="𝑳", textcolor=#000000, size=size.small, force_overlay=true)

plotshape(trend_changed and trend == -1 ? zl_basis : na, "Bearish Trend", 
     shape.labeldown, location.absolute, bearcolor, 
     text="𝑺", textcolor=#ffffff, size=size.small, force_overlay=true)

// Background signal lines
bgcolor(show_bg_lines ? 
     (ta.crossover(trend, 0) ? bullcolor : 
      ta.crossunder(trend, 0) ? bearcolor : na) : na)

// Color candles based on trend
barcolor(paint_candles ? 
     (trend == 1 ? bullcolor : 
      trend == -1 ? bearcolor : na) : na)

//              ╔════════════════════════════════╗              //
//              ║             ALERTS             ║              //
//              ╚════════════════════════════════╝              //

alertcondition(ta.crossover(trend, 0),
     title="Zero Lag Signals Long",
     message="Zero Lag Signals Long {{exchange}}:{{ticker}}")

alertcondition(ta.crossunder(trend, 0),
     title="Zero Lag Signals Short",
     message="Zero Lag Signals Short {{exchange}}:{{ticker}}")

//              ╔════════════════════════════════╗              //
//              ║           CREATED BY           ║              //
//              ╚════════════════════════════════╝              //

// ██████╗ ██╗   ██╗ █████╗ ███╗   ██╗████████╗     █████╗ ██╗      ██████╗  ██████╗ 
//██╔═══██╗██║   ██║██╔══██╗████╗  ██║╚══██╔══╝    ██╔══██╗██║     ██╔════╝ ██╔═══██╗
//██║   ██║██║   ██║███████║██╔██╗ ██║   ██║       ███████║██║     ██║  ███╗██║   ██║
//██║▄▄ ██║██║   ██║██╔══██║██║╚██╗██║   ██║       ██╔══██║██║     ██║   ██║██║   ██║
//╚██████╔╝╚██████╔╝██║  ██║██║ ╚████║   ██║       ██║  ██║███████╗╚██████╔╝╚██████╔╝
// ╚══▀▀═╝  ╚═════╝ ╚═╝  ╚═╝╚═╝  ╚═══╝   ╚═╝       ╚═╝  ╚═╝╚══════╝ ╚═════╝  ╚═════╝
