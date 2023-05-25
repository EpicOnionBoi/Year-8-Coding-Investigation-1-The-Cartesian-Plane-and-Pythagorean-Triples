import random # imports stuff
import math
from pytimedinput import timedInput

triples = [ # the list of pythagorean triples
[3, 4, 5],
[5, 12, 13],
[8, 15, 17],
[7, 24, 25],
[20, 21, 29],
[12, 35, 37],
[9, 40, 41],
[28, 45, 53],
[11, 60, 61],
[33, 56, 65],
[16, 63, 65],
[48, 55, 73],
[13, 84, 85],
[36, 77, 85],
[39, 80, 89],
[65, 72, 97],
[20, 99, 101],
[60, 91, 109],
[15, 112, 113],
[44, 117, 125],
[88, 105, 137],
[17, 144, 145],
[24, 143, 145],
[51, 140, 149],
[85, 132, 157],
[119, 120, 169],
[52, 165, 173],
[19, 180, 181],
[57, 176, 185],
[104, 153, 185],
[95, 168, 193],
[28, 195, 197],
[133, 156, 205],
[84, 187, 205],
[21, 220, 221],
[140, 171, 221],
[60, 221, 229],
[105, 208, 233],
[120, 209, 241],
[32, 255, 257],
[23, 264, 265],
[96, 247, 265],
[69, 260, 269],
[115, 252, 277],
[160, 231, 281],
[161, 240, 289],
[68, 285, 293],
[207, 224, 305],
[136, 273, 305],
[25, 312, 313],
[75, 308, 317],
[204, 253, 325],
[36, 323, 325],
[175, 288, 337],
[180, 299, 349],
[225, 272, 353],
[27, 364, 365],
[76, 357, 365],
[252, 275, 373],
[135, 352, 377],
[152, 345, 377],
[189, 340, 389],
[228, 325, 397],
[40, 399, 401],
[120, 391, 409],
[29, 420, 421],
[87, 416, 425],
[297, 304, 425],
[145, 408, 433],
[203, 396, 445],
[84, 437, 445],
[280, 351, 449],
[168, 425, 457],
[261, 380, 461],
[31, 480, 481],
[319, 360, 481],
[93, 476, 485],
[44, 483, 485],
[155, 468, 493],
[132, 475, 493],
[217, 456, 505],
[336, 377, 505],
[220, 459, 509],
[279, 440, 521],
[308, 435, 533],
[92, 525, 533],
[341, 420, 541],
[33, 544, 545],
[184, 513, 545],
[165, 532, 557],
[396, 403, 565],
[276, 493, 565],
[231, 520, 569],
[48, 575, 577],
[368, 465, 593],
[240, 551, 601],
[35, 612, 613],
[105, 608, 617],
[336, 527, 625],
[429, 460, 629],
[100, 621, 629],
[200, 609, 641],
[315, 572, 653],
[300, 589, 661],
[385, 552, 673],
[52, 675, 677],
[37, 684, 685],
[156, 667, 685],
[111, 680, 689],
[400, 561, 689],
[185, 672, 697],
[455, 528, 697],
[260, 651, 701],
[259, 660, 709],
[333, 644, 725],
[364, 627, 725],
[108, 725, 733],
[407, 624, 745],
[216, 713, 745],
[468, 595, 757],
[39, 760, 761],
[481, 600, 769],
[195, 748, 773],
[273, 736, 785],
[56, 783, 785],
[432, 665, 793],
[168, 775, 793],
[555, 572, 797],
]

player1 = { # stores coordinates of player 1
    "xcoords": random.randrange(-800,800,1),
    "ycoords": random.randrange(-800,800,1)
}

player2 = { # stores coordinates of player 2
    "xcoords": random.randrange(-800,800,1),
    "ycoords": random.randrange(-800,800,1)
}

destination = { # stores coordinates of the destination
    "xcoords": random.randrange(-800,800,1),
    "ycoords": random.randrange(-800,800,1)
}

def distance(player,destination): # calculates the distance between a player and the destination
    run = (player["xcoords"]-destination["xcoords"])**2
    rise = (player["ycoords"]-destination["ycoords"])**2
    distance = math.sqrt(run+rise)
    distance = round(distance,1)
    return distance

def midpoint(player1,player2): # finds the midpoint of the 2 players
    x = (player1["xcoords"]+player2["xcoords"])/2
    y = (player1["ycoords"]+player2["ycoords"])/2
    x = round(x,1)
    y = round(y,1)
    midpoint = [x,y]
    return midpoint

def gradient(player,destination): # finds the gradient of a player and the destination
    if player["ycoords"] >= destination["ycoords"]:
        rise = player["ycoords"]-destination["ycoords"]
        if player["xcoords"] >= destination["xcoords"]:
            run = player["xcoords"]-destination["xcoords"]
        else:
            run = destination["xcoords"]-player["xcoords"]
    else:
        rise = destination["ycoords"]-player["ycoords"]
        if player["xcoords"] >= destination["xcoords"]:
            run = player["xcoords"]-destination["xcoords"]
        else:
            run = destination["xcoords"]-player["xcoords"]
    gradient = rise/run
    gradient = round(gradient,1)
    return gradient

def info(player1,player2,destination): # prints out the information about the 3 entities
    print("The coordinates of player 1 are:",player1["xcoords"],",",player1["ycoords"])
    print("The coordinates of player 2 are:",player2["xcoords"],",",player2["ycoords"])
    print("The coordinates of the destination are:",destination["xcoords"],",",destination["ycoords"])
    print("The distance between player 1 and the destination is",distance(player1,destination))
    print("The distance between player 2 and the destination is",distance(player2,destination))
    print("The midpoint between the 2 players is",midpoint(player1,player2))
    print("The gradient of the line between player 1 and the destination is",gradient(player1,destination))
    print("The gradient of the line between player 2 and the destination is",gradient(player2,destination))

def move(triples): # calculates the movement of the player
    units, toolong = timedInput("How many units do you want to move? ", timeout=10) # asks for input with 10 second timer
    if toolong: # if the player takes too long, a random move will be made
            units = random.randrange(5, 400, 1)
            print("Took too long, buddy. You are moving",units,"units.")
    units = int(units)
    direction, tooloong = timedInput("In which direction do you want to move? ", timeout = 10) # asks for input with 10 second timer
    if tooloong: # if the player takes too long, a random move will be made
            direction = random.randrange(1, 8, 1)
            print("Took too long, buddy. You are moving in direction", direction)
    direction = int(direction)
    for e in triples: # finds the largest possible hypotenuse in regards to the units specified by the user
        if e[2] > units:
            print(hypotenuse)
            break
        hypotenuse = e
    shortside = hypotenuse[0] # creates variables for the shorter and medium side of the pythagorean triple
    longside = hypotenuse[1] 
    if direction == 1: # manages the directions (will be explained in more detail in presentation)
        x = longside
        y = shortside
    elif direction == 2:
        x = shortside
        y = longside
    elif direction == 3:
        x = -shortside
        y = longside
    elif direction == 4:
        x = -longside
        y = shortside
    elif direction == 5:
        x = -longside
        y = -shortside
    elif direction == 6:
        x = -shortside
        y = -longside
    elif direction == 7:
        x = shortside
        y = -longside
    elif direction == 8:
        x = longside
        y = -shortside
    return x, y # returns the changes in coordinates

def buff(destination, player1, player2): # checks to see if anyone has won
    player1_destination = distance(player1,destination) # checks distance between the 3 entities
    player2_destination = distance(player2,destination)
    players = distance(player1,player2)
    if player1_destination < 10: # if any of the distances are less than 10, it will return true. Otherwise, it will return false
        return True
    elif player2_destination < 10:
        return True
    elif players < 10:
        return True
    else:
        return False

P1WIN = False # makes 2 booleans to see if a player has won
P2WIN = False
while P1WIN == False and P2WIN == False: # this while loop runs while neither player has won yet. This is also the piece of codes that puts everything above together
    info(player1,player2,destination) # prints info on all the entities
    print("Player 1's turn:") # player 1's turn
    newcoords = move(triples)
    player1["xcoords"] = player1["xcoords"]+newcoords[0]
    player1["ycoords"] = player1["ycoords"]+newcoords[1]
    if buff(destination, player1, player2): # sees if player 1 has won
        P1WIN = True
    info(player1,player2,destination) # prints info again
    print("Player 2's turn:") # player 2's turn
    newcoords = move(triples)
    player2["xcoords"] = player2["xcoords"]+newcoords[0]
    player2["ycoords"] = player2["ycoords"]+newcoords[1]
    if buff(destination, player1, player2): # sees if player 2 has won
        P2WIN = True
    info(player1,player2,destination) # prints information again
if P1WIN == True: 
    print("Player 1 has won!")
else:
    print("Player 2 has won!")
