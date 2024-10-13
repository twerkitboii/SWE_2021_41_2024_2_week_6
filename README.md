# SWE_2021_41_2024_2_week_6
___
### Week 4 Assignment
#### Week 4 repository link
- Link
>https://github.com/twerkitboii/SWE_2021_41_2024_2_week_4
#### Week 4 Code
<pre>
<code>
```python
def isHappy(n):
    if n>2^31-1:
        return 0
    def get_next(number):
        total_sum = 0
        while number > 0:
            digit = number % 10
            total_sum += digit ** 2
            number //= 10
        return total_sum

    seen = set()

    while n != 1 and n not in seen:
        seen.add(n)
        n = get_next(n)

    return n == 1


n = int(input('Input: '))
if isHappy(n):
    print("True")
else:
    print("False")
```
</code>
    
</pre>

- Code Description
> - This code was made to check whether the number recieved from by input is a happy number or not.
> - I first checked whether the number was out of range, and then followed the method at the task description.
> - When the calculation is completed, I checked whether the result is 1 and if it is 1, I made the code to print out true, and if not, continue.
> - If the calculated result is a number that was already done before, I made it stop. 
___
### Week 5 Assignment
<pre><code>
docker exec ossp-container cat /etc/os-release
PRETTY_NAME="Ubuntu 24.04.1 LTS"
NAME="Ubuntu"
VERSION_ID="24.04"
VERSION="24.04.1 LTS (Noble Numbat)"
VERSION_CODENAME=noble
ID=ubuntu
ID_LIKE=debian
HOME_URL="https://www.ubuntu.com/"
SUPPORT_URL="https://help.ubuntu.com/"
BUG_REPORT_URL="https://bugs.launchpad.net/ubuntu/"
PRIVACY_POLICY_URL="https://www.ubuntu.com/legal/terms-and-policies/privacy-policy"
UBUNTU_CODENAME=noble
LOG0=ubuntu-logo
</code>
</pre>

<pre><code>
docker exec ossp-container git --version
git version 2.43.0
</code></pre>

<pre><code>
docker exec ossp-container python3 —-version
Python 3.12.3
</code></pre>

<pre><code>
docker inspect --format="{{ «HostConfig-Binds }}" ossp-container
[./ossp_host_dir:/mnt/ossp_container_dir]
</code></pre>
