JavaScript�ؼ���thisʼJS�ű��ܹ�����ʹ������ؼ��ֵ������Ľ�ֵ���ݸ�������
��������������һ����ҳ�����û���������֮�󣬵���һ��alert��Ȼ����ת��href������ָ����ҳ

HTML��
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>JavaScript�е�this����</title>
    <script type="text/javascript" src="js/script.js"></script>
</head>
<body>
    <p style="text-algin:center;">
        ��ã��������ȥ<a id="redirect" href="http://www.mybry.com/products/store/list.html">�����̵�</a>
    </p>
</body>
</html>
```
JS��
```
window.onload = initAll;
function initAll(){
    document.getElementById("redirect").onclick = initRedirect;
}
function initRedirect(){
    alert("�����Ҵ����ľ����̳ǣ���ӭ���ʣ�");
    window.location = this;
    return false;
}
```
[������ʾ](http://sandbox.runjs.cn/show/mp2pnrda)

����ܻ���Ҫ���������в�û�������ض�����ҳ��������this�ؼ��ֵ�����֮һ��this��������ɵĹ���֮һ�Ǵ�HTML���ӻ��URL��Ҳ����a��ǩ��href���ԣ������ڲ������ַ�ʽ������Ժ�ű���Ϊָ��������ҳ������Ǿ����̵�ҳ�棬�Ͳ����޸�JS��ʵ���ϣ�������WEBվ���ϵ��������Ӷ����������ͬ��JS���룬��һ�д��붼���Զ������Ӧ��hrefֵ��
����д����һ���ô�������û�������������JavaScript�����������JS��,��ô��ֻ�����HTMLҳ�棬������ʾalert��ʾ�������ǵ������ʱ������һ���������������ҳ�棬���ᷢ������û���κ����⡣
����������һ��switch/case���ӣ���������ҳ�棺
![Paste_Image.png](../image/160318/js-this/1.png)
HTML��
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>JavaScript�е�this����</title>
    <script type="text/javascript" src="js/script.js"></script>
</head>
<body>
    <h2>���ö���ͼ��</h2>
    <form action="#">
        <input type="button" id="Java" value="Java" />
        <input type="button" id="JavaScript" value="JavaScript" />
        <input type="button" id="MySQL" value="MySQL" />
        <input type="button" id="Html" value="HTML5" />
    </form>
</body>
</html>
```
JS:
```
window.onload = initAll;
function initAll(){
    document.getElementById("Java").onclick = viewDetail;
    document.getElementById("JavaScript").onclick = viewDetail;
    document.getElementById("MySQL").onclick = viewDetail;
    document.getElementById("Html").onclick = viewDetail;
}
function viewDetail(){
    console.log("this.id="+this.id);
    switch(this.id){
        case "Java" : 
            alert("��Java����Ա���������Ȿ�������д�ģ����ҵ��̵��ۼ�30Ԫ��");
            break;
        case "JavaScript" : 
            alert("��JavaScript���Ծ��⡷�Ȿ����Yahoo��һλ����ʦд�ģ����ҵ��̵��ۼ�15Ԫ��");
            break;
        case "MySQL" : 
            alert("��MySQL���źܼ򵥡��Ȿ�鸽�����̣���������ʵûʲô�����ˣ������ҵ��̵��ۼ�28Ԫ��");
            break;
        case "Html" : 
            alert("��HTML5�ؼ����Ȿ����ͼ��ϵͳ��ͼ�飬�ǳ�ֵ��ӵ�У������ҵ��̵��ۼ�25Ԫ�����ķǳ��ã�");
            break;
        default : 
            alert("û���Ȿ��");
    }
}
```
[������ʾ](http://sandbox.runjs.cn/show/wflrmken)

ֱ����this.id��Ϊswitch�Ĳ���Ҳ�ǿ��Եġ�

ԭ�����ӣ�[http://www.mybry.com/?p=407](http://www.mybry.com/?p=407)