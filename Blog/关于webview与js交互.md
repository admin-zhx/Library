
webview��js������Ҫ���
	``` webview.getSetting().setJavaScriptEnable(true);```
�������ã�
	``` webView.addJavascriptInterface(new Object(), "call");```
	

* html����java���� ����
	** E/Web Console: Uncaught TypeError: Object [object Object] has no method 'toString'**
	
	��Android4.2�Ժ�İ汾��Ҫ�ڵ��õķ���ǰ��ע����� ``  @JavascriptInterface ``
	
	```
		class Object {  
			@JavascriptInterface  
			public String toString() { return "callObject"; }			
		}  
	```


* JAVA��JS����ע������

	1��Java ���� js ����ĺ�����Ч�ʲ����Ǻܸߡ�����Ҫ200ms���Ұɡ��������Ժ�ǿ�����顢�����ٶȺ������˽��ܡ�
	��jsȥ��Java�ķ������ٶȺܿ졢50ms���ҡ����Ծ�����js����Java����
	2��Java ���� js �ĺ�����û�з���ֵ�������˾Ϳ��Ʋ�����
	3��Js ���� Java �ķ���������ֵ������ַ�������ᷢ������ַ����� native �ġ�ת�� locale �Ĳ�������ʹ�á�ʹ�� toLocaleString() �����Ϳ����ˡ���������������ٶȲ����졢ת�����ַ�������ܶࡢ����ܺķ�ʱ��
	4����ҳ�о�����Ҫʹ��jQuery��ִ��������Ҫ5-6�롢���ʹ��ԭ����jsдҵ��ű��������������ٶȡ������û�����	

	
�ο�ʵ�����ӣ�http://blog.csdn.net/ithomer/article/details/8737999