BIN = mqtt_broker
INC = 	-Iinclude
		
SRC = $(wildcard *.c jpg_lib/*.c)
OBJS = $(patsubst %.c,%.o,$(SRC))

CC = arm-none-linux-gnueabi-gcc -lpthread -ldl
LINUX_DIR = /home/welcome/Documents/v3s/qt/linux-3.4/include
CFLAGS := -I $(LINUX_DIR) $(INC) 
LDFLAGS = -L/home/welcome/Documents/v3s/qt/linux-3.4/lib \
			-L./lib/

$(BIN):$(OBJS)
	$(CC) $(LDFLAGS) $(CFLAGS) -o $@ $^

clean:
	rm $(OBJS) $(BIN)