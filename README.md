t = int(input("تعداد آزمایش‌ها: "))


for _ in range(t):

    try:
        n = int(input())
        k = int(input())
    except ValueError:

        n = 100
        k = 2


    people = list(range(1, n + 1))


    index = 0


    while len(people) > 1:
        index = (index + k - 1) % len(people)
        people.pop(index)


    print(people[0])
