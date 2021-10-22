# Work that I'm Most Proud of

I still amaze myself at what I am able to do with a computer, especially since my mind was set on the fact that IT was going to be too hard for me. The following block of code is from a python project that reads a `.txt` file and generates data from the file.
```
def calc_sum(filepath, fp):
    sum = 0
    for n in fp:
        n = n.strip()
        nums = n.split(',')
        for ns in nums:
            sum = sum + int(ns)
    print("Sum:",sum)

def calc_count(filepath, count):
    with open(filepath) as fp:
        for line in fp:
            if line != "\n":
                count+=1
        print("Count:",count)

def calc_avg(filepath, average, total):
    length = 0
    fp = open(filepath)
    for line in fp:
        amount = float(line)
        total += amount
        length += 1
    average = total / length
    print("Average:", average)

def calc_maxminrng(filepath, total, count):
    num_list = []
    with open(filepath) as fp:
        for line in fp:
            number = int(line)
            total += number
            count += 1
            num_list.append(number)
        max_num = max(num_list)
        min_num = min(num_list)
        rng = max_num - min_num
        print("Max:", max_num)
        print("Min:", min_num)
        print("Range:", rng)
def main():
    total = 0
    count = 0
    average = 0
    while True:
        try:
            filepath = input("File name: ")
            fp = open(filepath)
            calc_sum(filepath, fp)
            calc_count(filepath, count)
            calc_avg(filepath, average, total)
            calc_maxminrng(filepath, total, count)
            response = input("Do you want to perform another calculation? (Yes/No) ")
            if (response == "Yes"):
                print("")
                continue
            if (response == "No"):
                break
        except Exception as error:
            print(error)
main()
```
While this code may look messy to someone more advanced in this topic, I'm proud to say that I was able to create something like this and hope that someday I'll be able to create something that is actually useful to someone, something that improves everyday life.

[Back to Home](README.md)
