# BTC-ml
BTC-ml is a web app for a ANN trading system. BTC-ml helps us to predict Bitcoin price movemnet.

 <p>BTC-ml uses Artificial neural network to predict movement of Bitcoin.</p>
            <p>The data that was used to train ANN derived from Candle stick data and volume traded in BTC.</p>
            <img src="https://a.c-dn.net/c/content/dam/publicsites/igcom/uk/images/ContentImage/BULLISH%20BEARISH%20CANDLESTICK-150620.jpg" style="max-width: 300px;">
            <p>BTC-ml uses 34 features that were extracted from candlestick data. 3 different time frames were used 1 day, 4 hours and 1 hour.</p>
            <p>1 minute time frame had too many noise, so it didn't give good results.</p>
            <p>We utilze few tehnical indicators used by financial experts.</p>
            <ul>
                <li>
                    <b>Moving average (MA)</b>
                    <p>The numerical average value of the stock prices over a period of time.</p>
                    <p>MAS, MAL : short-term and long-term moving average, respectively.</p>
                    <p>Short-term average uses last 50 data points and long-term uses last 200.</p>
                </li>
                <li>
                    <b>Golden-cross and dead-cross</b>
                    <p>States that MAS crosses MAL upward and downward, respectively.</p>
                </li>
                <li>
                    <b>Moving average convergence and divergence (MACD)</b>
                    <p>A momentum indicator that shows the relationship between MAS and MAL.</p>
                    <p>MACD = MAS − MAL</p>
                </li>
                <li>
                    <b>Relative strength index (RSI)</b>
                    <p>An oscillator that indicates the internal strength of a single stock.</p>
                    <p>\[RSI = 100 - { 100 \over 1 + U/D}\]</p>
                    <p>U, D : An average of upward and downward price changes, respectively.</p>
                </li>
                <li>
                    <b>Stochastics</b>
                    <p>An indicator that compares where a stock price closed relative to its price range  over a given time period</p>
                    <p>\[K = { x(t) − L \over H − L }*100\]</p>
                    <p>H, L = The highest and the lowest price in a given time period.</p>
                    <p>D = Moving average of %K</p>
                </li>
            </ul>
            <p>With those finantial indicators 34 features were genterated, there are 17 formulas. Some features used the same formula but different data.</p>
            <ul>
                <li><p>X1 = (x(t) − x(t − 1))/x(t − 1)</p></li>
                <li><p>X2 = (x(t) − xl(t))/xh(t) − xl(t)</p></li>
                <li><p>X3 = (MA(t) − MA(t − 1))/MA(t − 1)</p></li>
                <li><p>X4 = (MAS(t) − MAL(t))/MAL(t)</p></li>
                <li><p>X5 = (x(t) − MA(t))/MA(t)</p></li>
                <li><p>X6 = x(t) − min(x(t), x(t − 1), . . . , x(t − 5))</p></li>
                <li><p>X7 = x(t) − max(x(t), x(t − 1), . . . , x(t − 5))</p></li>
                <li><p>X8 = # of days since the last golden-cross</p></li>
                <li><p>X9 = # of days since the last dead-cross</p></li>
                <li><p>X10 = the profit while the stock has risen or fallen continuously</p></li>
                <li><p>X11 = # of days for which the stock has risen or fallen continuously</p></li>
                <li><p>X12 = MACD(t)</p></li>
                <li><p>X13 = MACD(ema(t))</p></li>
                <li><p>X14 = RSI(t)</p></li>
                <li><p>X15 = %K (t)</p></li>
                <li><p>X16 = %D(t)</p></li>
                <li><p>X17 = %K (t) − %K (t − 1 )</p></li>
                <li><p>X18 = %D(t) − %D(t − 1 )</p></li>
            </ul>
        </div>
