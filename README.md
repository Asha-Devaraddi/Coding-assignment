# Coding-assignment
Solution file
def maximumEarnings(jobs):
    n = len(jobs)
    jobs.sort(key=lambda x: x[1])
    task = 0
    earnings = 0
    last_job_end = 0
    for i in range(n):
        if jobs[i][0] >= last_job_end:
            task += 1
            earnings += jobs[i][2]
            last_job_end = jobs[i][1]
    return [n - task, earnings]
n= int(input("Enter the number of Jobs"))
print("Enter job start time, end time, and earnings")
n1 = int(input())
n2 = int(input())
n3 = int(input())
n4= int(input())
n5 = int(input())
n6 = int(input())
n7= int(input())
n8 = int(input())
n9 = int(input())
jobs =  [[n1, n2, n3], [n4, n5, n6], [n7, n8, n9]]
a = maximumEarnings(jobs)

print("The number of tasks and earnings available for others Task: "+str(a[0]))
print("Earnings: "+str(a[1]))

