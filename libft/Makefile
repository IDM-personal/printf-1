# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Makefile                                           :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: parmarti <parmarti@student.42.fr>          +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2020/06/29 16:20:52 by parmarti          #+#    #+#              #
#    Updated: 2020/07/21 11:10:55 by parmarti         ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

NAME		= libft.a

SRCS		= ft_memset.c ft_bzero.c ft_memcpy.c ft_memccpy.c ft_memmove.c ft_memchr.c ft_memcmp.c \
		  	  ft_nbrlen.c ft_strlen.c ft_strlcpy.c ft_strlcat.c ft_strchr.c ft_strrchr.c ft_strnstr.c ft_strcmp.c ft_strncmp.c \
		  	  ft_atoi.c ft_isalpha.c ft_isdigit.c ft_isalnum.c ft_isascii.c ft_isprint.c ft_tolower.c ft_toupper.c \
		  	  ft_calloc.c ft_strdup.c ft_substr.c ft_strjoin.c ft_strtrim.c ft_split.c ft_itoa.c ft_strmapi.c \
		  	  ft_putchar_fd.c ft_putstr_fd.c ft_putendl_fd.c ft_putnbr_fd.c

BONUS		= ft_lstnew_bonus.c ft_lstadd_front_bonus.c ft_lstsize_bonus.c ft_lstlast_bonus.c ft_lstadd_back_bonus.c \
		  	  ft_lstdelone_bonus.c ft_lstclear_bonus.c ft_lstiter_bonus.c ft_lstmap_bonus.c

LBRS		= libft.h

OBJS		= $(SRCS:.c=.o)

OBJS_BONUS	= $(BONUS:.c=.o)

CC			= cc

RM			= rm -rf

AR			= ar rcs

CFLAGS		= -Wall -Wextra -Werror

NORME		= norminette -R CheckForbiddenSourceHeader

all:		$(NAME)

$(NAME):	$(OBJS)
			$(AR) $(NAME) $(OBJS)

bonus:		$(OBJS) $(OBJS_BONUS)
			$(AR) $(NAME) $(OBJS) $(OBJS_BONUS)

.c.o:
			$(CC) $(CFLAGS) -c $< -o $(<:.c=.o)

clean:
			$(RM) $(OBJS) $(OBJS_BONUS)

fclean:		clean
			$(RM) $(NAME)

re:			fclean all

norme:		
			$(NORME) $(SRCS) $(BONUS) $(LBRS)

.PHONY:		all bonus clean fclean re norme

