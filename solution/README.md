
<h1 align="center">
Codeforces Round 859 (Div. 4) 
</h1>



![.](../i.png)

### Input :
```yaml
2
5 5
2 2 1 3 2
2 3 3
2 3 4
1 5 5
1 4 9
2 4 3
10 5
1 1 1 1 1 1 1 1 1 1
3 8 13
2 5 10
3 8 10
1 10 2
1 9 100
```

### Output :
```yaml
YES
YES
YES
NO
YES
NO
NO
NO
NO
YES
```

![.](../i1.png)





<h1 align="center">
Solution 🍑🍆 
</h1>

```cpp
#include<bits/stdc++.h>
using namespace std;

#define ll long long

int main() {
   
    ll t, n, q, temp, l, r, k;
    vector<ll> v, v2;
    
    cin >> t;
    while(t--) {
        v.clear();
        ll sum = 0;
        cin >> n >> q;
        for (ll i = 0; i < n; i++) {
            cin >> temp;
            v.push_back(temp);
        }
        while(q--) {
            sum = 0;
            v2 = v;
            cin >> l >> r >> k;
            for (ll j = l-1; j < r; j++) {
                v2[j] = k;
            }
            for (ll i = 0; i < v2.size(); i++) {
                sum += v2[i];
            }
            sum % 2 == 1 ? cout << "YES" << endl : cout << "NO" << endl;
        }
    }
    return 0;
}    
```

### Input :
```yaml
2
5 5
2 2 1 3 2
2 3 3
2 3 4
1 5 5
1 4 9
2 4 3
10 5
1 1 1 1 1 1 1 1 1 1
3 8 13
2 5 10
3 8 10
1 10 2
1 9 100
```

### Output :
```yaml
YES
YES
YES
NO
YES
NO
NO
NO
NO
YES

```
