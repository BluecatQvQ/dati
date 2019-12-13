```javascript
export default {
    addNum({commit,state},id){
        commit('REMBER_ANSWER',id);
        if (state.itemNum < state.itemDetail.length) {
            commit('ADD_ITEMNUM',1)
        }
    },
    startTimer({commit}){
        commit('REMBER_TIME');
    },
    initializeData({commit}){
        commit('INITIALIZE_DATA');
    }
}
```