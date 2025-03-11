# Leetcode-1358

# C++

class Solution {
public:
    int numberOfSubstrings(string s) {
        int count=0,a=0,b=0,c=0,i=0,j=0,n=s.length();
        while(j<n)
        {
            if(s[j]=='a')a++;
            else if(s[j]=='b')b++;
            else c++;
            while(i<j&&a!=0&&b!=0&&c!=0)
            {
                count++;
                count+=(n-j-1);
            if(s[i]=='a')a--;
            else if(s[i]=='b')b--;
            else
            c--;
            i++;
            }
            j++;
        }
        return count;
    }
};

# Java

class Solution {
    public int numberOfSubstrings(String s) {
        int count = 0, a = 0, b = 0, c = 0, i = 0, j = 0, n = s.length();
        while (j < n) {
            if (s.charAt(j) == 'a') a++;
            else if (s.charAt(j) == 'b') b++;
            else c++;

            while (i < j && a != 0 && b != 0 && c != 0) {
                count++;
                count += (n - j - 1);
                if (s.charAt(i) == 'a') a--;
                else if (s.charAt(i) == 'b') b--;
                else c--;
                i++;
            }
            j++;
        }
        return count;
    }
}

# Python

class Solution:
    def numberOfSubstrings(self, s: str) -> int:
        count, a, b, c, i, j, n = 0, 0, 0, 0, 0, 0, len(s)
        while j < n:
            if s[j] == 'a':
                a += 1
            elif s[j] == 'b':
                b += 1
            else:
                c += 1

            while i < j and a != 0 and b != 0 and c != 0:
                count += 1
                count += (n - j - 1)
                if s[i] == 'a':
                    a -= 1
                elif s[i] == 'b':
                    b -= 1
                else:
                    c -= 1
                i += 1

            j += 1
        return count
