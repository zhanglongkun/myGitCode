#���ɸ���Makefile��
# 1. ��ֵ��PROJ���������ɵĿ�ִ���ļ���
PROJ   = WebCrawler
# 2. ��ֵ��OBJS��ִ���ļ�������������.o�ļ�
OBJS   = StrKit.o       \
         Log.o          \
         Configurator.o \
         MultiIo.o      \
         PluginMngr.o   \
         Hash.o         \
         BloomFilter.o  \
         Url.o          \
         UrlQueues.o    \
         Socket.o       \
         Thread.o       \
         DnsThread.o    \
         SendThread.o   \
         RecvThread.o   \
         WebCrawler.o   \
         Main.o
#��ֵ�൱���������Ⱥ��Ҳ�����
CXX    = g++
LINK   = g++
RM     = rm -rf
CFLAGS = -c -Wall -I. -D_DEBUG
LIBS   = -ldl -lpthread #-levent

#�����ӡ�
# ���������滻�����ͬ�� ��(#define), $^ ���������� <==> $(OBJS)
$(PROJ): $(OBJS)
	$(LINK) $^ $(LIBS) -o ../bin/$@

#�����롿
# .o������.cpp , �˴��� $^ �������������ļ����е�.cpp
.cpp.o:
	$(CXX) $(CFLAGS) $^

#������ָ�$ make clean
clean:
	$(RM) ../bin/$(PROJ) $(OBJS) *.gch