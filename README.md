# C++-homework

To calculate how many words in a article

```Cpp
#include <bits/stdc++.h>

#define all(a) (a).begin(),(a).end()

using namespace std;

int main(){
	string str;
	getline(cin,str);
	stringstream ss(str);
	map<string,int> mymap;
	while(ss >> str) mymap[str]++;
	vector<pair<int,string>> sorted;
	for(auto i:mymap) sorted.push_back({-i.second, i.first});
	sort(all(sorted));
	for(int i=0; i<5; i++) cout << sorted[i].second << ' ' << (sorted[i].first)*(-1) << '\n';
    	return 0;
}
```
