Getting Started
===============

Este documento irá mostrar algumas definições e facilidades do Sistema e Site da
Automação IOT.

Guia Básico
-----------

O site possui variedades de opções para serem utilizados, porém este guia visa apresentar um **quickstart** para que 
você consiga de maneira rápida e prática criar os seus dispositivos e recursos, bem como realizar a programação de eventos 
para os recursos entre outros.

**Definições**

* :ref:`Dispositivo`
* :ref:`Recurso`
* :ref:`Recurso de Entrada`
* :ref:`Recurso de Saída`
* :ref:`Fluxo de Entrada e Saída`
* :ref:`Links Externos`

**Funcionalidades**

* :ref:`Tipos de Recurso`
* :ref:`Subtipos de Recurso`
* :ref:`Métrica`
* :ref:`Criando Dispositivo e Recurso`
* :ref:`Programar Evento`
* :ref:`Mapa`

.. _Dispositivo:

Dispositivo
~~~~~~~~~~~

É representado pelo conjunto de aparelhos ou mecanismos que possuam capacidade de integração e comunicação via API com a base de dados IOT, bem como realizar a comunicação e processamento com os recursos 
de entrada/saída.

.. _Recurso:

Recurso
~~~~~~~

É representado pelo conjunto de recursos de entrada/saída que possuam capacidade de integração e comunicação com dispositivo.

.. _Recurso de entrada:

Recurso de Entrada
~~~~~~~~~~~~~~~~~~

É representado pelo conjunto de recursos que recebem informações da base de dados IOT.

.. tip:: Tipos de Recursos de Entrada.
   
   - Relé.
   - Sirene.

.. _Recurso de Saída:

Recurso de Saída
~~~~~~~~~~~~~~~~

É representado pelo conjunto de recursos que enviam informações para a base de dados IOT.

.. tip:: Tipos de Recursos de Saída.
   
   - Temperatura.
   - Umidade.
   - Distância

.. _Fluxo de Entrada e Saída:

Fluxo de Entrada e Saída
~~~~~~~~~~~~~~~~~~~~~~~~

**Fluxo de Entrada**

.. image:: imagem/fluxo-entrada.png
    :align: center   

Um recurso de entrada recebe informações da base de dados IOT através da API. Em geral estes recursos são conectados a dispositivos 
que necessitam de algum estímulo para serem ativados. 

.. tip:: Mundo Real.
   Sistema embarcado recebe ordem para ativação de um relé. Este relé poderá acionar um equipamento elétrico associado a este, tais como :
    - Motor, 
    - Lâmpada, 
    - Sirene, 
    - Tomada etc.

**Fluxo de Saída**

.. image:: imagem/fluxo-saida.png
    :align: center   

Um recurso de saída envia informações para a base de dados IOT através da API. 
Em geral estes recursos são conectados a dispositivos que informam ou reportam dados concretos que representam alguma coisa no mundo real. 

.. tip:: Mundo Real.
   Sistema embarcado fornece dados de temperatura e umidade do ambiente. Dados são armazenados,   parametrizados e disponibilizados para acesso a usu�rios com permiss�o.
    - Temperatura, 
    - Umidade, 
    - Distância, 
    - Luminosidade etc.

.. _Tipos de Recurso:

Tipos de Recurso
~~~~~~~~~~~~~~~~

Define o tipo associado ao recurso, que poderá ser de Entrada ou Saída.

.. _Subtipos de Recurso:

Subtipos de Recurso
~~~~~~~~~~~~~~~~~~~

Define o Subtipo associado ao recurso de acordo com o seu tipo. 

.. tip:: Recurso do tipo Entrada teremos os subtipos.
    
    - Binário,
    - Dado Bruto,
    - Digital, etc.


.. tip:: Recurso do tipo Saída teremos os subtipos.

    - Estado,
    - Unidade,
    - Dado Bruto, etc.

.. _Métrica:

Métrica
~~~~~~~

Define a forma (label) de como o Feed será apresentado na opção *Gerenciar Feed*.
Esta forma de apresentação tem a relação direta com o *Tipo e Subtipo de Recurso*.

.. tip:: Exemplo de Métrica para Tipo **Entrada** e Subtipo Binário
                       
    - Para o valor do Feed 0 cadastrar na métrica *Desligado* será apresentado o label *Desligado* em Gerenciar Feed.
    - Para o valor do Feed 1 cadastrar na métrica *Ligado* será apresentado o label *Ligado* em Gerenciar Feed.

.. tip:: Exemplo de Métrica para Tipo **Saída** e Subtipo Estado

    - Para o valor do Feed 0 cadastrar na métrica *Vazio* será apresentado o label *Vazio* em Gerenciar Feed.
    - Para o valor do Feed 1 cadastrar na métrica *Metade* será apresentado o label *Metade* em Gerenciar Feed.
    - Para o valor do Feed 2 cadastrar na métrica *Cheio* será apresentado o label *Cheio* em Gerenciar Feed.

.. _Criando Dispositivo e Recurso:

Criando Dispositivo e Recurso
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Para podermos iniciar o processo de comunicação de disposto e recurso para com a base de dados IOT, 
teremos que cria-los antes em nosso site. Para isso basta acessarmos as opções  de cadastrar dispositivo e 
cadastrar recurso.

**Cadastrar Dispositivo**

.. image:: imagem/cadastro-device.png
    :align: center   

- Tempo Presença: Tempo em minutos (Lifetime) que demonstra o status do dispositivo, que poderá ser Conectado ou Desconectado.
- Time Zone: Que irá ajustar a data/hora conforme o GMT do dispositivo.
- Latitude e Longitude :  São relativos as coordenadas onde encontra-se o dispositivo (que poderá ser visualizado através do Mapa). Inicialmente estes campos estar�o preenchidos com as coordenadas do endere�o cadastrado pelo usu�rio (op��o Usu�rio � Alterar cadastro), caso o endere�o seja vazio, as coordenadas ser�o preenchidas com as coordenadas do provedor de IP do usu�rio. Para alterarmos manualmente as coordenadas do dispositivo, deveremos clicar na opção Mapa, e posicionarmos o marcador na localização desejada.

.. image:: imagem/cadastro-mapa.png
   :align: center   

**Cadastrar Recurso** 

.. image:: imagem/cadastro-resource.png
    :align: center   

- Tempo Presença: Tempo em minutos (Lifetime) que demonstra o status do recurso, que poderá ser Conectado ou Desconectado.
- Tipo: Recurso de Entrada ou Saída.
- Subtipo: Subtipo para recurso do tipo Entrada ou Saída. 

.. _Programar Evento:

Programar Evento
~~~~~~~~~~~~~~~~

**Evento Ativo**

Opção responsável por realizar a programação de eventos para os recursos do tipo Entrada (Ativo) e Saída (Passivo).

Recursos de entrada poderão ter a sua programação de ativar e desativar realizado através da seguinte opção (Evento Ativo):

.. image:: imagem/evento-ativo.png
    :align: center   

**Evento Passivo**

Recursos de Saída poderão ter a sua programação de ativar e desativar um recurso qualquer de Entrada, 
de acordo com o valor de Saída associado ao Operador Lógico definido  através da seguinte opção (Evento Passivo):

.. image:: imagem/evento-passivo.png
    :align: center   

.. _Mapa:

Mapa
~~~~

.. image:: imagem/mapa.png
    :align: center   

Através da opção *Mapa* poderá ser visualizado todos os dispositivos cadastrados por conta individual.

No canto superior direito do *Mapa* temos a opção de filtragem de visualização dos dispositivos,
poderá ser filtrado para ser apresentado dispositivos Ativados e/ou Desativados. 

Ao abrir o mapa não será apresentado nenhum dispositivo, pois o filtro não estará selecionado.

Marcadores em *Vermelho* estará representando os dispositivos Desativados.

Marcadores em *Verde* estará representando os dispositivos Ativados.


.. _Links Externos::

Links Externos
~~~~~~~~~~~~~~

Documentação API_ Automação-IOT.

.. _API: http://api-automacaoiot.readthedocs.io/pt/latest/

Documentação ESP8266 SDK_. 

.. _SDK: http://api-automacaoiot.readthedocs.io/pt/latest/

Documentação Biblioteca_ ESP8266 SDK. 

.. _Biblioteca: http://api-automacaoiot.readthedocs.io/pt/latest/