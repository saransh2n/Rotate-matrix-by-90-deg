// Rotate-matrix-by-90-deg

// A basic understanding and operation of STL vector implementing the same


class Solution {
public:
    void rotate(vector<vector<int>>& matrix) {
    /*vector<vector<int>> temp = matrix;
    int m= matrix.size();
    int n=matrix[0].size();

    for(int i=0; i<m; i++){
        int k=m-1;
        for(int j=0; j<n; j++){
          matrix[i][j]=temp[k][i];
          k--;  
         }
    } */
    int n = matrix.size();
    for(int i=0; i<n; i++){
        for(int j=0; j<i; j++){
            swap(matrix[i][j], matrix[j][i]);
        }
    }
    for(int i=0; i<n; i++){
            reverse(matrix[i].begin(), matrix[i].end());
    }

    }
};
