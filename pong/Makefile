# Compiler
CXX = clang++

# Compiler flags
CXXFLAGS = -std=c++20 -I/user/local/include

# Linker flags
LDFLAGS = -L/usr/local/lib -lSDL2

# Source files
SRCS = Game.cpp Main.cpp

# Object files
OBJS = $(SRCS:.cpp=.o)

# Executable name
EXEC = game

# Default target
all: $(EXEC)

# Rule to link the executable
$(EXEC): $(OBJS)
	$(CXX) $(CXXFLAGS) -o $@ $^ $(LDFLAGS)

# Rule to compile source files to object files
%.o: %.cpp
	$(CXX) $(CXXFLAGS) -c $< -o $@

# Clean up generated files
clean:
	rm -f $(OBJS) $(EXEC)

# Phony targets
.PHONY: all clean
