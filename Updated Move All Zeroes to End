class Solution {
  public:
    void pushZerosToEnd(vector<int>& arr) {
        int cnt = 0;
        for(int i = 0;i<arr.size();i++){
            if(arr[i] == 0)cnt++;
            if(arr[i] and cnt){
                swap(arr[i-cnt], arr[i]);
            }
        }
    }
};
