# NotePad
Android Mid-term operation


### 阅读NotePad的源代码并做如下扩展：

##### 基本要求：

  NoteList中显示条目增加时间戳显示
  
  添加笔记查询功能（根据标题查询）
    
![](https://github.com/wall-chen/NotePad/blob/master/images/Notepad_P3.PNG)  
##### 附加功能：
  

  更改记事本的背景
![](https://github.com/wall-chen/NotePad/blob/master/images/Notepad_P1.PNG)  

  UI美化
![](https://github.com/wall-chen/NotePad/blob/master/images/Notepad_P2.PNG)  




从数据库中读取的cursor中获取笔记列表对应的颜色数据，并设置笔记颜色

```
public class MyCursorAdapter extends SimpleCursorAdapter {
    public MyCursorAdapter(Context context, int layout, Cursor c,
                           String[] from, int[] to) {
        super(context, layout, c, from, to);
    }
    @Override
    public void bindView(View view, Context context, Cursor cursor){
        super.bindView(view, context, cursor);
        从数据库中读取的cursor中获取笔记列表对应的颜色数据，并设置笔记颜色
        int x = cursor.getInt(cursor.getColumnIndex(NotePad.Notes.COLUMN_NAME_BACK_COLOR));
        /**
         * 白 255 255 255
         * 黄 247 216 133
         * 蓝
