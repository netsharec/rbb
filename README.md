# Replace Bilibili bofqi #

<span style="font-size: 60px; font-weight: bold; line-height: 80px;">[��˽���ű���ҳ](http://tiansh.github.io/rbb/)</span>

<span style="font-size: 60px; font-weight: bold; line-height: 80px;">[���ֱ�Ӱ�װ�ű�](http://tiansh.github.io/rbb/replace_bilibili_bofqi.user.js)</span>

�û����Ʋ��ű���ҳ����ҳ����Ҫ���ܽű���һЩʵ��ԭ��

[����һЩbilibili��Ƶ����������wiki��](https://github.com/tiansh/rbb/wiki)

���ű����緢����userscripts.org��վ�ϣ�176946�������ǵ�����վ�����ȶ��ط��ʣ������ƶ�����github�ϡ�����2.21��ǰ����ʷ�汾�����Ե�userscripts���ҵ���

## ��ȡcid ##

��ȡ��Ƶ��ַ��Ҫ��ȡcid����������ǰ���õĻ�ȡcid��;����

### ͨ��API��ȡ ###

<code>http://api.bilibili.com/view?type=json&id={aid}&batch=1&appkey={appkey}</code>

�������⡢������cid����ҳ�������Ϣ��<br />
��Ϣ��ȫ��������Ƶ�����ƣ��ڲ���Ҫ��ϸ��Ϣʱ�������ȿ���ʹ��������;����

### ͨ��pagelist��ȡ ###

<code>http://www.bilibili.tv/widget/getPageList?aid={aid}</code>

����cid����ҳ���⡣

### ͨ��HTML5�ӿڻ�ȡ ###

<code>http://www.bilibili.tv/m/html5?aid={aid}&page={pid}</code>

���޵�����ҳ���ɻ�ȡcid��

### ͨ��flash������ȡ ###

flash������"cid"��"\*-cid"�����ṩcid

## ��ȡaid ##

<code>http://interface.bilibili.com/player?id=cid:{cid}</code>

����ͨ��cid��ȡaid

## ������Ƶ�Ʋ�cid ##

�������ֱ�ӻ�ȡcid���ῼ��ͨ�����ڵ���Ƶ��cid��ȡaid��

�����ʵ���ǻ���cid[i] > cid[j] ���ҽ��� aid[i] > aid[j]�ڴ��������³�����Ϊ����ġ�

��ǰ�ű���ʵ�ַ����ǣ�
* ��ȡǰ��������Ƶ��cid
  * �����ж����ҳ����Ƶ
  * ��ȡ������6����Ƶ��cid���򲻳���12����Ƶ��������ȡʧ�ܣ�
* ������Щcid�ƶ�cid���ܵ�����
  * ������߶�û�л�ȡ��cid�򱨸�ʧ��
  * ���һ��û�л�ȡ��cid��ʹ����һ�����/С��cid��Ϊ���
  * ȥ���Ҳ������������ֶ�С�ģ��������Ҳ��������ֶ����
  * �ҵ����ߵ���λ��������һ���������λ������Ĳ��ֿ���
  * ��������������������һ����������Ĳ��ֿ���
  * ���������������������Ϊ����Ҫ��cid�������Χ��
* ����cid���ܵ����䳢��
  * ���м������߽��г���
  * ���������32��������ʲ����ҵ���Ƶ�����
    * ʹ���˻��������¿���ʵ�����Ѿ������˸������Ƶ
  * ����ҵ���ĳ����ҳ֮�����ҵ���ҳ����4��6����Ƶ����ʧ����ֹͣ
* �������õ�aid���б�


## ����Ƿ������������ ##

<code>http://interface.bilibili.com/playurl?cid={cid}</code>

�������succ��suee��˵���ɹ�


## �޸���ҳȫ���͸��������� ##

��ο���http://static.hdslb.com/js/page.arc.js


## ��ȡ�·�ר��������� ##

�ο���<br />
<code>http://api.bilibili.com/spview?spid={spid}&season\_id={season\_id}&bangumi=1</code><br />
<code>http://api.bilibili.tv/sp?spid={spid}</code>

spview�е�bangumi����Ϊ0/1�����������������绹�������Ƶ��

������API�ƺ�����Ҫappkey�����ӡ���


## �������·��б� ##

�·��б������˲�����Ƶ�������Ҫ�������·��б���Ҫͨ���ֻ��ļ��ط�ʽ��ȡ��
<code>http://api.bilibili.com/list?pagesize=24&type=json&page=1&ios=0&order=default&appkey={appkey}&platform=ios&tid=33</code>��

## ������Ƶ��Ϣ ##

### �������Զ���ȫ ###

������������ /av\d+/ ��ʽ���ִ�������ʾ��Ӧ��Ƶ�ı��⡣�����ô˻�ȡ��Ƶ����

<code>http://www.bilibili.tv/suggest?term=av{{aid}}&jsoncallback={{callback}}&rnd={{random}}&\_={{date}}</code>

������ JSONP ��ʽ�ģ�Ҫע�����callback�ǲ���ʡ�ģ������ֱ�Ӳ��������ݡ�

### ����ҳ��ʹ�õĽӿ� ###

����ӿڿ��Ի�ȡ������Ƶ����Ϣ���в�ȷ��ʲô�����¿��Ի�ȡ����ʲô����²��С�

<code>http://www.bilibili.tv/html/arc/{{aid}}.html</code>

���ص��� HTML ��Ƭ�Ρ�

## �ű��ӿ� ##

�����ű�ʹ�ñ��ű��ӿڵķ���

```javascript
// ��������һ������Ϊ��Ӧ�ĺ�������String����"ping"��"getCid"��
// ��������ɸ�����Ϊ������������Ĳ���
var rbb = function () {
  if (!unsafeWindow.replaceBilibiliBofqi) unsafeWindow.replaceBilibiliBofqi = [];
  unsafeWindow.replaceBilibiliBofqi.push(Array.apply(Array, arguments));
  return unsafeWindow.replaceBilibiliBofqi.constructor.name !== 'Array';
};
```

���ϴ����ṩ�˵��ñ��ű��ӿڵķ�������rbb('ping', function () { alert('replace bilibili bofqi loaded!'); });���Լ�鱾�ű��Ƿ��ѱ����ء�

�ű��ṩ�Ľӿڰ������нӿ� 

### ping ###

* ��鱾�ű��Ƿ񱻼��أ���ע�᱾�ű�������ʱ�Ļص�����
* ������callback �ص�������Function��
  * ������ ���ޣ�

### getAid ###

* ͨ��cid���aid��pid��Ϣ
* ������cid ��Ƶ��chatid����529622��Number��
  * onsucc �ɹ���ȡʱ�Ļص�������Function��
  * ������id һ������aid��pid�Ķ�����{"aid":314,"pid":1}��
  * onerror ��ȡʧ�ܵĻص�������Function��
  * ���������ޣ�

### cid ###

* ��ȡ��ǰ��Ƶ��cid
* ������callback ����cid�Ļص�������Function��
  * ������null ��ǰ�޷���ȡ������Ƶҳ�棨�ɺ��ԣ���ȡ��������µ��ûص�������
  * ������cid ��Ƶ��cid��Number��
  * ��һЩ��������滻�˵�ǰҳ��Ĳ������󣬿��ܻᷴ�����øûص�����

### getCid ###

* ͨ��aid��pid��ȡcid
* ������id һ������aid��articlecid��av�ţ���pid��pageid���Ķ���
       ��{"aid":314,"pid":1}����{"aid":314,"pid":null}����Object��
  * onsucc �ɹ���ȡʱ�Ļص�������Function��
  * ������cid��Number������529622����Ӧ��һ�ֲ�������
          ��һ��pid��cid�ļ�ֵ���飨Object������{"1":529622}����Ӧ�ڶ��ֲ�����
  * onerror ��ȡʧ��ʱ�Ļص�������Function��
  * ���������ޣ�
  * methods ��ȡcidʹ����Щ��������Щ������˳��String���ɵ�Array��
  * ���ܵ�ȡֵ��
    * "direct" ֱ�ӻ�ȡ�����ܰ���HTML5��AssDown��PlayList�ȣ�
    * "api" ͨ��API��ȡ
    * "undirect" ��ӻ�ȡ��ͨ��������Ƶ��cid�²⣩
    * "cached" ��ȡ���棨���֮ǰ��ȡ�����û�û�н��û��棩

˵�������ֻ��Ҫһ����ҳ����pid���գ������и���ļ��ʻ�ȡ��cid�����ֻ��Ҫ��ǰ��Ƶ��cid����ʹ��cid�ӿڡ�


### replaced ###

* ע�ᷢ���滻�������¼�ʱ�Ļص�����
* ������callback �滻������ʱ�ص���Function��
  * ������true ��ʾ�¼��Ѿ���ע��
  * ������cid ���������滻ʱ���ã���������Ƶ��cid��Number��

### added ###

* ע��������۵������Ϣʱ�Ļص�����
* ������callback �滻������ʱ�ص���Function��
  * ���������ޣ�

