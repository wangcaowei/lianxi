<script>
export default defineComponent({
  methods:{
    // 冒泡排序
    bubbleSort(arr){
      var i=arr.length,j;
      var changeVal;
      //循环（数组长度）次，依次找到（数组长度）个最大值
      while(i>0){
        for(j=0;j<i-1;j++){
          if(arr[j]>arr[j+1]){
            changeVal=arr[j];
            arr[j]=arr[j+1];
            arr[j+1]=changeVal
          }
        }
        i--
      }
      return arr
    },
    // 插入排序
    insertSort(arr){
      //循环待排序的数组元素（下表为1开始）
      //第一个数据（下表为0），由于插入序列刚开始，有序表中没有记录，可以直接添加到有序表中
      for(var i=1;i<arr.length;i++){
        var changeVal=arr[i];//存储当前用于比较的值
        for(var j=i;j>0&&arr[j-1]>changeVal;j--){
          arr[j]=arr[j-1]
        }
        arr[j]=changeVal
      }
      return arr
    },
    // 选择排序
    selectionSort(arr){
      for(var i=0;i<arr.length-1;i++){
        for(var j=i+1;j<arr.length;j++){
          if(arr[i]>arr[j]){
            // var changeVal=arr[i]
            // arr[i]=arr[j]
            // arr[j]=changeVal
            [arr[i],arr[j]]=[arr[j],arr[i]]
          }
        }
      }
      return arr
    }
  }
})
</script>
