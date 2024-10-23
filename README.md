<strategy>
    <trade_parameters>
        <market>R_100</market>
        <trade_type>CALL</trade_type>
        <stake>1</stake>
        <duration>5</duration>
    </trade_parameters>

    <purchase_conditions>
        <condition>
            <indicator>RSI</indicator>
            <period>14</period>
            <level>30</level>
            <operator>GREATER_THAN</operator>
        </condition>
    </purchase_conditions>

    <restart_conditions>
        <loss_multiplier>2</loss_multiplier>
        <max_consecutive_losses>5</max_consecutive_losses>
    </restart_conditions>
</strategy>
<strategy>
    <trade_parameters>
        <market>R_100</market>
        <trade_type>PUT</trade_type>
        <stake>1</stake>
        <duration>5</duration>
    </trade_parameters>

    <purchase_conditions>
        <condition>
            <indicator>CCI</indicator> <!-- Commodity Channel Index for overbought/oversold -->
            <period>20</period>
            <level>100</level>
            <operator>LESS_THAN</operator>
        </condition>
    </purchase_conditions>

    <restart_conditions>
        <win_stake_decrease>1</win_stake_decrease>
        <loss_stake_increase>1</loss_stake_increase>
        <max_consecutive_losses>5</max_consecutive_losses>
    </restart_conditions>
</strategy>
<strategy>
    <trade_parameters>
        <market>R_100</market>
        <trade_type>CALL</trade_type>
        <stake>1</stake>
        <duration>5</duration>
    </trade_parameters>

    <purchase_conditions>
        <condition>
            <indicator>MACD</indicator> <!-- Moving Average Convergence Divergence -->
            <period_fast>12</period_fast>
            <period_slow>26</period_slow>
            <signal_period>9</signal_period>
            <operator>CROSS_ABOVE</operator>
        </condition>
    </purchase_conditions>

    <restart_conditions>
        <win_stake_increase>1</win_stake_increase>
        <max_consecutive_losses>3</max_consecutive_losses>
    </restart_conditions>
</strategy>
