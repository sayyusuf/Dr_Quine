# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Makefile                                           :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: ysay <ysay@student.42.fr>                  +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2022/01/10 15:44:43 by ysay              #+#    #+#              #
#    Updated: 2022/10/02 17:10:36 by ysay             ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

NAME= $(NAME1) $(NAME2) $(NAME3)
NAME1= Colleen
NAME2= Grace
NAME3= Sully

_SRC= $(patsubst %,%.s,$(NAME))
_OBJ= $(_SRC:.s=.o)

SDIR=
ODIR=
IFLAG= -I./

SRC= $(patsubst %,$(SDIR)%,$(_SRC))
OBJ= $(patsubst %,$(ODIR)%,$(_OBJ))
INC= $(patsubst %,$(IFLAG)%,$(_IDIR))

CC= clang

FLAGS= -Wall -Wextra -Werror

.PHONY: all clean fcelan re

all: $(NAME)

$(NAME): $(OBJ) $(EXLIB)
	$(CC) $(FLAGS) $(INC) $(ODIR)$@.o $(EXLIB) -o $@
$(ODIR)%.o : $(SDIR)%.c 
	$(CC) $(FLAGS) $(INC) -c  $< -o $@


clean:
	rm -rf $(OBJ) $(NAME3)_* $(NAME2)_kid.s
fclean: clean
	rm -rf $(NAME)
re: fclean all
