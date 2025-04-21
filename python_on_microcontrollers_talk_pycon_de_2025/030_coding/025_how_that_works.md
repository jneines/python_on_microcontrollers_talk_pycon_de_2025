# How does that work

:::::{grid} 2 2 2 2

::::{card}

Computer - Task Version

:::{code} Python
x0 = .25

max_iterations = 10

x = x0

for iteration in range(max_iterations):
    x = x**2 + x0
    if abs(x) > 4:
        break

print(iteration)
:::

::::

::::{card}

Microcontroller - Tasklet Edition

:::{code} Python
x0 = .25

max_iterations = 10

pc = 0
iteration = 0

while True:
    if pc == 0:
        registers[0] = x0
        registers[1] = max_iterations
        registers[2] = iteration
        
        pc += 1
        continue
    elif pc == 1:
        x0 = registers[0]
        x = x0
        registers[3] = x
        
        pc += 1
        continue
    elif pc == 2:
        x = registers[3]

        # perform 1st part of the calculation
        x = x*x

        registers[3] = x
        pc += 1
        continue
    elif pc == 3:
        x0 = registers[0]
        x = registers[3]
        iteration = registers[2]

        # perform 2nd part
        x += x0
        iteration += 1

        registers[3] = x
        registers[2] = iteration
        pc += 1
        continue
    elif pc == 4:
        x = registers[3]
        
        if abs(x) > 4:
            pc = 6 # end condition
            continue
        
        pc += 1
        continue
    elif pc == 5:
        iteration = registers[2]
        max_iterations = registers[1]
        
        if iteration == max_iterations:
            # some sort of break
            pc = 6 
            continue
        
        # goto pc==2 case. This makes the loop
        pc = 2
        continue
    elif pc == 6:
        # end condition
        iteration = registers[2]
        break

print(iteration)
:::

::::

:::::
