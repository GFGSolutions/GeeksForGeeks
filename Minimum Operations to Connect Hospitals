class DisjointSet{
    vector<int> parent, size;
    public:
        DisjointSet(int n){
            parent.resize(n);
            size.resize(n);
            for(int i=0;i<n;i++) {
                parent[i]=i;
                size[i]=1;
            }
        }
        int find(int node){
            if(node==parent[node]) return node;
            return parent[node]=find(parent[node]);
        }
        bool unionBySize(int u, int v){
            int pu=find(u);
            int pv=find(v);
            if(pu==pv) return false;
            if(size[pu]>size[pv]){
                size[pu]+=size[pv];
                parent[pv]=pu;
            } else {
                size[pv]+=size[pu];
                parent[pu]=pv;
            }
            return true;
        }
        int countComp(){
            int c=0;
            for(int i=0;i<parent.size();i++){
                if(parent[i]==i) c++;
            }
            return c;
        }
};
class Solution {
  public:
    int minConnect(int V, vector<vector<int>>& edges) {
        int e=edges.size();
        if(e<V-1) return -1;
        DisjointSet dsu(V);
        for(auto ed:edges){
            dsu.unionBySize(ed[0],ed[1]);
        }
        int ct=dsu.countComp();
        return ct-1;
    }
};
