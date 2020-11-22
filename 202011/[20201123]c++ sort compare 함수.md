# [C++] Sort Compare 함수

vector<vector<int>> or vector<pair<int, int>> 에서 첫 번째는 그대로 두고, 두 번째 값만 수정해야 할때 사용.

```
bool compare(vector<int> p1, vector<int> p2)
{
    return p1[1] < p2[1];
}
```

단순하지만, 엄청난 발전인듯...

