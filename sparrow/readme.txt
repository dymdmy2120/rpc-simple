��ģ�齫sparrow��Ŀ�ĸ�����ģ��ϲ���һ��jar ���а����˸���ģ���еİ�����
�޸�ע�⣺

1) ������µ�ģ�飬Ҫ��POM��maven-shade-plugin��<artifactSet>�����<include>

2) ������µ���չ�㣬Ҫ��POM��maven-shade-plugin����<transformer>

������ ��չ�������ļ� ������

$ find . -wholename */META-INF/sparrow/* -type f | grep -vF /test/ | awk -F/ '{print $NF}' | sort -u
com.dynamo.sparrow.cache.CacheFactory
com.dynamo.sparrow.common.compiler.Compiler
com.dynamo.sparrow.common.extension.ExtensionFactory
...and so on...
