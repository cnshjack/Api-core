

# ����ʹ��˵��

## `srcĿ¼`
Դ����Ŀ¼�µ�srcĿ¼����֮Ϊ`srcĿ¼`
`srcĿ¼`Ŀ¼����3���ļ�:
- `index.php`
- `index.config.php`
- `.htaccess`

## `webĿ¼`
��linuxϵͳ�£�����git clone�������뵽ĳ��Ŀ¼�£�����һ��Ҫֱ�ӷ���`DOC_ROOT`�¡�
�����`srcĿ¼`�µ�`index.php`��`.htaccess`��2���ļ��÷������ӵ�`DOC_ROOT`�µ�ĳĿ¼�¡�
����`DOC_ROOT/api/v1.0/`Ŀ¼�¡�
��Ŀ¼��֮Ϊ`webĿ¼`��

ע����windowsϵͳ�£�����û�з������ӣ�`srcĿ¼`��`webĿ¼`ͨ����һ���ġ�

## �����ļ�
��linuxϵͳ�£�����`srcĿ¼`��`webĿ¼`��һ��ʱ��
��`webĿ¼`�£��ɸ���һ��`index.config.php`�����޸�Ϊ�Լ����������ݡ�
��ʵ���޸����ö������޸�gitԭ����Ŀ¼����ļ���

## api��URI��ʽ
API_ROOT_PATH/$api/$call/?xxxxxx
RewriteRule ^([a-zA-Z]\w+)/([a-zA-Z]\w+)$ index.php?api=$1&call=$2&%{QUERY_STRING}	[L]
$1:$api
$2:$call

## api��Ӧ��php�ļ�
ÿ��api��Ӧһ��/apis/Ŀ¼�µ�һ���ļ���
������`srcĿ¼/apis`��Ҳ������`webĿ¼/apis`�¡�
`webĿ¼/apis`���ȡ�

## api URI��php�ļ��Ķ�Ӧ
Ҫ��
php�ļ�����`"/api_$api.php"`
������`"class_$api"`
������`public static function $call() {}`