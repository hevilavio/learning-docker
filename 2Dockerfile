FROM debian

RUN /bin/echo "Teste 123!!"

ADD teste.txt /tmp/
VOLUME /dados
ENV dburl="oracle:teste 123"

RUN ["sh", "-c", "cat /tmp/teste.txt"]
RUN ["sh", "-c", "echo $dburl"]

ENTRYPOINT ["/bin/echo", "Teste entrypoint. Quando o comando finalizar, o container finaliza junto."]

