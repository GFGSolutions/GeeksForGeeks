// User Template For C++

class Solution {
  public:
    int countValid(int n, vector<int>& arr) {
        vector<bool> allowed(10, false);
        for (int d : arr) allowed[d] = true;
        int f = 0, f0 = 0;
        for (int d = 0; d < 10; ++d) {
            if (!allowed[d]) {
                f++;
                if (d != 0) f0++;
            }
        }
        if (f == 0) {
            int total = 1;
            for (int i = 1; i < n; ++i) total *= 10;
            return 9 * total;
        }
        int total = 1;
        for (int i = 1; i < n; ++i) total *= 10;
        total *= 9;
        int forbidden_count = 0;
        if (f0 > 0) {
            forbidden_count = f0;
            for (int i = 1; i < n; ++i) forbidden_count *= f;
        }
        return total - forbidden_count;
    }
};
