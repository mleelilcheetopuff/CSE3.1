"""The function move(my_history, their_history) must return 'r', 'p', or 's'.
my_history and their_history are strings of the same length, perhaps length zero.
"""

strategy_name = "Rock first, then alternate paper and scissors"

def move(my_history, their_history):
    if (len(my_history) == 0):
        my_move = 'r'
    elif (len(my_history) % 2 == 0):
        my_move = 'p'
    else:
        my_move = 's'
    return my_move

def predict_their_move(their_history):
    return their_history[-1]


def foresight(next_move):
    if next_move == "r":
        return "p"
    elif next_move == "p":
        return "s"
    else:
        return "r"
