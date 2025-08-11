// User Template For C++

class Solution {
  public:
    vector<int> minMaxCandy(vector<int>& prices, int k) {
        int mn=0, mx=0;
        sort(prices.begin(), prices.end());
        int l=0, r=prices.size()-1;
        while(l<=r){
            mn+=prices[l];
            r-=k;
            l++;
        }
        l=0, r=prices.size()-1;
        while(l<=r){
            mx+=prices[r];
            l+=k;
            r--;
        }
        return {mn, mx};
    }
};
