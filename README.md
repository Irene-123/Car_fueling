# Car_fueling
The car fueling problem.
'''python

def min_refills(d, stops, dist_with_full_tank):
    num_refills = 0
    current_refills = 0
    last_refills = 0
    while current_refills <= d:
        last_refills = current_refills
        while (stops[current_refills + 1] - stops[last_refills]) <= dist_with_full_tank:
                current_refills = current_refills + 1
                if current_refills == (d - 1):
                    break
        if current_refills == last_refills:
            return "Impossible"
        if current_refills < (d - 1):
            num_refills = num_refills + 1
    return num_refills
    '''
  
