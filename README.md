# lab-7
numbers = [3, 15, 7, 22, 10, 8, 14]
with open("input.txt", "w") as f:
    for num in numbers:
        f.write(str(num) + " ")
with open("input.txt", "r") as f:
    content = f.read()
nums = list(map(int, content.split()))
condition = [num for num in nums if num > 9]
total = sum(condition)
with open("output.txt", "w") as f:
    for num in condition:
        f.write(str(num) + " ")
    f.write(f"\nSum: {total}")
print("Numbers greater than 9:", condition)
print("Sum:", total)
