CFLAGS = $(COMMONFLAGS) -Wall
LDFLAGS = $(COMMONFLAGS)

### Sources variables
SRC_DIR = ../src
INCS = -I../inc 
OBJS = $(patsubst %.c,%.o, $(notdir $(shell find $(SRC_DIR) -type f -name "*.c")))

### Output variables
EXE = hello-demo
OUT_DIR = ../target

### Rules
all: $(EXE)

$(EXE): $(OBJS)
	$(CC) $(LDFLAGS) -o $@ $(OBJS)
	@mkdir -p $(OUT_DIR)
	@mv $(EXE) $(OUT_DIR)

# Compile
%.o: $(SRC_DIR)/%.c
	$(CC) $(INCS) -c $(CFLAGS) $< -o $@

# Cleanup
clean:
	rm -f *.o
	rm -f $(OUT_DIR)/*
