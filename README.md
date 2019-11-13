# python_BaseballGame
#1
n, k = map(int, input().split())
total = 0
for i in range(1, n):
    if i % k == 0:
        total += i

print(total)

#2
n, k = map(int, input().split())
print("n :", n, "k :", k)
if k < 2 or k > 10:
    print("k는 2이상 10이하의 자연수 입니다.")
    exit(1)

arr = []
answer = 0
while n >= k:
    arr.append(n % k)
    n = n // k
arr.append(n)
arr.reverse()
answer = int(''.join(map(str, arr)))
print(answer)
