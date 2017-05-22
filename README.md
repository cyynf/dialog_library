# dialog_library
 <h3>仿IOS对话框：</h3><br> 

``` java
   new AlertDialog(this)
  .builder()
  .setTitle("提示")
  .setMsg("要放弃编辑的内容吗？")
  .setPositiveButton("确认放弃", new View.OnClickListener() {
       @Override
       public void onClick(View v) {
                           
       }
    })
  .setNegativeButton("取消", new View.OnClickListener() {
       @Override
       public void onClick(View v) {

       }
    })
  .show();
 ```

 ``` java
  new ActionSheetDialog(MenuActivity.this)
                        .builder()
                        .setTitle("注销后需要重新登录，确认要注销吗？")
                        .setCancelable(false)
                        .setCanceledOnTouchOutside(false)
                        .addSheetItem("确认", ActionSheetDialog.SheetItemColor.Red
                                , new ActionSheetDialog.OnSheetItemClickListener() {
                                    @Override
                                    public void onClick(int which) {
                                       
                                    }
                                }).show();
 ```             

 ``` java
ActionSheetDialog.OnSheetItemClickListener onSheetItemClickListener = new ActionSheetDialog.OnSheetItemClickListener() {
            @Override
            public void onClick(int which) {
               
        };
                                
  ActionSheetDialog actionSheetDialog = new ActionSheetDialog(MainActivity.this)
                        .builder();
                actionSheetDialog.setCancelable(false)
                        .setCanceledOnTouchOutside(false);
                actionSheetDialog.addSheetItem(""), ActionSheetDialog.SheetItemColor.Blue
                            , onSheetItemClickListener);
                actionSheetDialog.addCancelListener(new ActionSheetDialog.OnCancelListener() {
                    @Override
                    public void onCancel() {
                      
                    }
                });
                actionSheetDialog.show();
  ```  
  
 <h3> 动画加载对话框：</h3><br> 

 ``` java
 //初始化对话框<br>
ShapeLoadingDialog loadingDialog = new ShapeLoadingDialog(this);
 loadingDialog.setLoadingText("加载中...");
 //显示       
  loadingDialog.show();
  //隐藏
  loadingDialog.dismiss();
 ```
 
 <h3> 旋转加载对话框：</h3><br> 
 
 ``` java
  CustomProgress diaog;
  diaog = CustomProgress.show(this, "加载中...", true, null);
  diaog.dismiss();
 ```
