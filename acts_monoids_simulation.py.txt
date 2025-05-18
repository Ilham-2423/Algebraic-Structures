# Simulating basic monoid operation and simple S-act behavior

# Define a monoid with an identity element and binary operation
monoid_elements = [0, 1, 2]
identity = 0

def monoid_op(a, b):
    return (a + b) % 3  # Example: Z_3 addition

# Define an S-act: a set with a monoid acting on it
S_act = ['x', 'y', 'z']

def act_action(m, s):
    # Just a sample simulation: rotate the element based on m
    index = S_act.index(s)
    return S_act[(index + m) % len(S_act)]

# Simulate some actions
for m in monoid_elements:
    for s in S_act:
        print(f"{m} * {s} = {act_action(m, s)}")
