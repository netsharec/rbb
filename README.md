<span style="font-size: 60px; font-weight: bold; line-height: 80px;">[��˰�װ�ű�](http://tiansh.github.io/rbb/replace_bilibili_bofqi.user.js)</span>

<span style="font-size: 60px; font-weight: bold; line-height: 80px;">[��˽���ű���ҳ](http://tiansh.github.io/rbb/)</span>


# �ű��ӿ� #

�����ű�ʹ�ñ��ű��ӿڵķ���

<pre><code>// ��������һ������Ϊ��Ӧ�ĺ�������String����"ping"��"getCid"��
// ��������ɸ�����Ϊ������������Ĳ���
var rbb = function () {
  if (!unsafeWindow.replaceBilibiliBofqi) unsafeWindow.replaceBilibiliBofqi = [];
  unsafeWindow.replaceBilibiliBofqi.push(Array.apply(Array, arguments));
  return unsafeWindow.replaceBilibiliBofqi.constructor.name !== 'Array';
};</pre></code>

���ϴ����ṩ�˵��ñ��ű��ӿڵķ�������rbb('ping', function () { alert('replace bilibili bofqi loaded!'); });���Լ�鱾�ű��Ƿ��ѱ����ء�

�ű��ṩ�Ľӿڰ������нӿ� 

## ping ##

* ��鱾�ű��Ƿ񱻼��أ���ע�᱾�ű�������ʱ�Ļص�����
* ������callback �ص�������Function��
  * ������ ���ޣ�

## getAid ##

* ͨ��cid���aid��pid��Ϣ
* ������cid ��Ƶ��chatid����529622��Number��
  * onsucc �ɹ���ȡʱ�Ļص�������Function��
  * ������id һ������aid��pid�Ķ�����{"aid":314,"pid":1}��
  * onerror ��ȡʧ�ܵĻص�������Function��
  * ���������ޣ�

## cid ##

* ��ȡ��ǰ��Ƶ��cid
* ������callback ����cid�Ļص�������Function��
  * ������null ��ǰ�޷���ȡ������Ƶҳ�棨�ɺ��ԣ���ȡ��������µ��ûص�������
  * ������cid ��Ƶ��cid��Number��
  * ��һЩ��������滻�˵�ǰҳ��Ĳ������󣬿��ܻᷴ�����øûص�����

## getCid ##

* ͨ��aid��pid��ȡcid
* ������id һ������aid��articlecid��av�ţ���pid��pageid���Ķ���
       ��{"aid":314,"pid":1}����{"aid":314,"pid":null}����Object��
  * onsucc �ɹ���ȡʱ�Ļص�������Function��
  * ������cid��Number������529622����Ӧ��һ�ֲ�������
          ��һ��pid��cid�ļ�ֵ���飨Object������{"1":529622}����Ӧ�ڶ��ֲ�����
  * onerror ��ȡʧ��ʱ�Ļص�������Function��
  * ���������ޣ�
  * methods ��ȡcidʹ����Щ��������Щ������˳��String���ɵ�Array��
  * ���ܵ�ȡֵ��"direct" ֱ�ӻ�ȡ�����ܰ���API��HTML5��AssDown��PlayList�ȣ�
    * "undirect" ��ӻ�ȡ��ͨ��������Ƶ��cid�²⣩
    * "cached" ��ȡ���棨���֮ǰ��ȡ�����û�û�н��û��棩

˵�������ֻ��Ҫһ����ҳ����pid���գ������и���ļ��ʻ�ȡ��cid�����ֻ��Ҫ��ǰ��Ƶ��cid����ʹ��cid�ӿڡ�


## replaced ##

* ע�ᷢ���滻�������¼�ʱ�Ļص�����
* ������callback �滻������ʱ�ص���Function��
  * ������true ��ʾ�¼��Ѿ���ע��
  * ������cid ���������滻ʱ���ã���������Ƶ��cid��Number��

## added ##

* ע��������۵������Ϣʱ�Ļص�����
* ������callback �滻������ʱ�ص���Function��
  * ���������ޣ�