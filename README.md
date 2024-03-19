#include<bits/stdc++.h>
using namespace std;

using ll = long long;
using vect = vector<ll>;
using Map = map<ll,ll>;
using str = string;
using Set = set<ll>;
using Pair = pair<ll,ll>;
using priorq = priority_queue<ll>;

#define mod 1000000007
#define sort(a) sort(a.begin(),a.end())
#define rev(a) reverse(a.begin(),a.end())
#define pb push_back
#define print(a)  for(auto i:a){cout<<i;}cout<<endl;
#define  read(x) ll x;  cin >> x 
#define sread(s) str s; cin>>s
#define vread(ans,n) vector<ll>ans(n); for(ll i=0;i<n;i++){cin>>ans[i];}

ll power(ll x, ll y) {
    ll res = 1;
    while (y > 0) {
        if (y & 1) res = res * x;
        y >>= 1;
        x = x * x;
    }
    return res;
}

ll factorial(ll n) {
    if (n == 0 || n == 1) return 1;
    return n * factorial(n - 1);
}

ll gcd(ll a, ll b) {
    if (b == 0) return a;
    return gcd(b, a % b);
}

ll lcm(ll a, ll b) {
    return (a * b) / gcd(a, b);
}

ll binary_search(vect& arr, ll target) {
    ll left = 0, right = arr.size() - 1;
    while (left <= right) {
        ll mid = left + (right - left) / 2;
        if (arr[mid] == target) return mid;
        else if (arr[mid] < target) left = mid + 1;
        else right = mid - 1;
    }
    return -1;
}

void print_vector(vect& v) {
    for (auto num : v) {
        cout << num << " ";
    }
    cout << endl;
}

void print_map(Map& mp) {
    for (auto& [key, value] : mp) {
        cout << key << ": " << value << endl;
    }
}

int main() {
    // Your code here
    return 0;
}
