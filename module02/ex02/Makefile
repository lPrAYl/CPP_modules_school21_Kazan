NAME		=	fixed_two
SRCS		=	$(shell find . -name "*.cpp")
HDRS		=	$(shell find . -name "*.hpp")
OBJS		=	$(SRCS:.cpp=.o)

CC			=	clang++
CFLAGS		=	-std=c++98 -pedantic -Wall -Werror -Wextra -O2

GREEN		=	\033[32;1m
BLUE		=	\033[36;1m
PURPLE		=	\033[35;1m
RESET		=	\033[0m

all			:	$(NAME)

%.o			:	%.cpp
			$(CC) $(CFLAGS) -c -o $@ $<

$(NAME)		:	$(OBJS)
			$(CC) -o $@ $^

clean		:
			rm -rf $(OBJS)

fclean		:	clean
			rm -rf $(NAME)

re			:	fclean all

.PHONY		:	all clean fclean re test