# An example

:::::{grid} 2 2 2 2 

::::{card} Computer

    while True
        read sensor
        send data
        sleep some_time

- will be able to do other things in the meantime
- energy usage will hardly change during `sleep some_time`
- not suitable for battery use
::::


::::{card} Microcontroller

    at boot:
        read sensor
        send data
        set interrupt for wake_up after some_time
        enter deep_sleep mode

- is offline during actions
- energy use will be down to a minimum (typically $\mu$A range)
- ideal for battery use!

::::

:::::
