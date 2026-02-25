# ==========================================================
# 1) Statement:
# Add two numbers (10 and 20) using CPU Registers.
# ==========================================================

print("Example 1: Using Registers")

R1 = 10          # Load 10 into R1
R2 = 20          # Load 20 into R2
R3 = R1 + R2     # Add R1 and R2 and store in R3

print("Result =", R3)
print()


# ==========================================================
# 2) Statement:
# Add two numbers stored in memory using SI and DI.
# ==========================================================

print("Example 2: Using Memory with SI and DI")

memory = {
    "1000": 10,
    "1002": 20
}

SI = "1000"                  # Load address of first number
DI = "1002"                  # Load address of second number

R1 = memory[SI]              # Move value from [SI] into R1
R2 = memory[DI]              # Move value from [DI] into R2

RESULT = R1 + R2             # Add and store

print("Result =", RESULT)
print()


# ==========================================================
# 3) Statement:
# Add 10 and 20 using Stack (Pointer Register SP).
# ==========================================================

print("Example 3: Using Stack (SP)")

stack = []                   # Stack
SP = -1                      # Stack Pointer

# Push 10
R1 = 10
stack.append(R1)
SP += 1

# Push 20
R2 = 20
stack.append(R2)
SP += 1

# Pop values
R3 = stack.pop()
SP -= 1

R4 = stack.pop()
SP -= 1

R5 = R3 + R4                 # Add values

print("Result =", R5)
print()


# ==========================================================
# 4) Statement:
# Add two numbers from Data Segment using DS register.
# ==========================================================

print("Example 4: Using Data Segment (DS)")

DS = {
    "NUM1": 10,
    "NUM2": 20,
    "RESULT": 0
}

R1 = DS["NUM1"]              # Load first number
R2 = DS["NUM2"]              # Load second number

DS["RESULT"] = R1 + R2       # Store result in data segment

print("Result =", DS["RESULT"])
print()