# demoCode

def pair_sum_sorted_array(numbers, target):
    """
    Given a sorted array of integers in non-decreasing order, find two numbers in the array that add up to a specific target.
    The indices of these two numbers, denoted as index1 and index2, should be returned in a 1-indexed array [index1, index2].


 Args:
        numbers (List[int]): A sorted array of integers in non-decreasing order.
        target (int): The target number to find.

    Returns:
        List[int]: A 1-indexed array of the indices of the two numbers in the array that add up to the target.
    """
    left = 0
    right = len(numbers) - 1

    while left < right:
        current_sum = numbers[left] + numbers[right]

        if current_sum == target:
            return [left + 1, right + 1]
        elif current_sum < target:
            left += 1
        else:
            right -= 1

    return [-1, -1]

