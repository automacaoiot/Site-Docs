Funcionalidades
---------------

.. _Dispositivo:

Dispositivo
~~~~~~~~~~~

Para podermos iniciar o processo de comunicação do dispositivo para com a base de dados IOT,
deverá ser criado o dispositivo na Dashboard, opção **Cadastrar**.

.. image:: ../imagem/dashboard.png
    :align: center

Veremos a seguinte tela de cadastro:

**Cadastrar Dispositivo**

.. image:: ../imagem/cadastro-device.png
    :align: center

- Nome: Nome do Dispositivo.
- Descrição: Descrição do Dispositivo.
- Icone: Icone que será associado ao dispositivo, para apresentação no Mapa.
- Chave Pública: Chave Pública do Dispositivo, criado automaticamente, que será utilizada na programação do SDK.
- Chave Secreta: Chave Secreta do Dispositivo, criado automaticamente, que será utilizada na programação do SDK.
- Tempo Presença: Tempo em minutos (Lifetime) que demonstra o status do dispositivo, que poderá ser Conectado ou Desconectado.
- Situação: Dispositivo Ativado ou Desativado, no modo Desativado o dispositivo não irá se comunicar com a base de dados IOT.
- Time Zone: Que irá ajustar a data/hora conforme o GMT do dispositivo.
- Latitude e Longitude :  São relativos as coordenadas onde encontra-se o dispositivo (que poderá ser visualizado através do Mapa). Inicialmente estes campos estarão preenchidos com as coordenadas do endereço cadastrado pelo usuário (opção Usuário Alterar cadastro), caso o endereço esteja vazio, as coordenadas serão preenchidas com as coordenadas do provedor de IP do usuário. Para alterarmos manualmente as coordenadas do dispositivo, deveremos clicar na opção Mapa, e posicionarmos o marcador na localização desejada.
- Visibilidade: Quando Pública o dispositivo poderá ser visualizado por outros usuários, quando Privado somente poderá ser visualizado pelo seu proprietário.

**Localização Dispositivo no Mapa**

O botão Mapa no cadastro do dispositivo, possibilita a localização deste no Mapa em coordenadas de Latitude e Longitude.

.. image:: ../imagem/cadastro-mapa.png
   :align: center

.. _Recurso:

Recurso
~~~~~~~

Para podermos iniciar o processo de criação do recurso na base de dados IOT,
deverá ser criado o recurso na Dashboard, opção **Cadastrar**.

.. image:: ../imagem/dashboard-recurso.png
    :align: center

Veremos a seguinte tela de cadastro:

**Cadastrar Recurso**

.. image:: ../imagem/cadastro-resource.png
    :align: center

- Nome: Nome do Recurso.
- Descrição: Descrição do Recurso.
- Tempo Presença: Tempo em minutos (Lifetime) que demonstra o status do recurso, que poderá ser Conectado ou Desconectado.
- Situação: Recurso Ativado ou Desativado, no modo Desativado o recurso não irá se comunicar com a base de dados IOT.
- Tipo: Recurso de Entrada, Saída ou Entrada/Saída.
- Subtipo: Subtipo do recurso (Binário, Digital, Estado, Unidade, Bruto, etc.).

.. _Subtipo:

Subtipo
~~~~~~~

Para podermos iniciar o processo de criação de subtipos na base de dados IOT,
deverá ser acessado a opção **Subtipo** na Dashboard.

.. image:: ../imagem/dashboard-subtipo.png
    :align: center

Veremos a seguinte tela:

.. image:: ../imagem/subtipo-menu.png
    :align: center

Onde poderemos cadastrar/Editar e Apagar subtipos. Os subtipos nativos não poderão ser alterados ou apagados.

.. _Métrica:

Métrica
~~~~~~~

A opção de métrica do recurso, está associado ao **Tipo de Dado** do Subtipo vinculado ao recurso.

.. note:: Tipos de Dados

    - Integer,
    - Float,
    - Boolean,
    - String.

.. note:: O sistema IOT possui os seguintes subtipos já cadastrados

    - Binário,
    - Digital,
    - Estado,
    - Unidade,
    - Bruto.

.. important:: Teremos algumas combinações possíveis, que representam os Subtipos IOT.

  - Boolean x Binário,
  - String x Estado,
  - Integer x Digital,
  - Float x Digital,
  - etc.



.. _Evento Ativo:

Evento Ativo
~~~~~~~~~~~~

Opção responsável por realizar a programação de eventos para os recursos do tipo Entrada ou Entrada/Saída (Ativo).

Recursos de entrada poderão ter a sua programação de ativar e desativar realizado através da seguinte opção (Evento Ativo):

.. image:: ../imagem/dashboard-ativo.png
    :align: center

Tela de cadastro de evento ativo:

.. image:: ../imagem/cadastro-ativo.png
    :align: center

- Data Inicio Evento: Data de início da execução do evento.
- Hora Inicio Evento: Hora de início da execução do evento.
- Data Final Evento: Data de término da execução do evento.
- Hora Final Evento: Hora de término da execução do evento.
- Valor Inicial Evento: Valor que será armazenado no Feed do recurso associado, por ocasião do início da execução do evento.
- Valor Final Evento: Valor que será armazenado no Feed do recurso associado, por ocasião do término da execução do evento.
- Situação Evento: Evento Ativado ou Desativado, no modo Desativado o evento não será executado.
- Ativa Sensor Diariamente: Evento será executado todos os dias, na Hora Inicio Evento e será finalizado na Hora Final Evento.

.. _Evento Passivo:

Evento Passivo
~~~~~~~~~~~~~~
Opção responsável por realizar a programação de eventos para os recursos do tipo Saída (Passivo).

Recursos de Saída poderão ter a sua programação de ativar e desativar um recurso qualquer de Entrada,
de acordo com o valor de Saída associado ao Operador Lógico definido  através da seguinte opção (Evento Passivo):

.. image:: ../imagem/dashboard-passivo.png
    :align: center

Tela de cadastro de evento passivo:

.. image:: ../imagem/cadastro-passivo.png
    :align: center

- Nome do Recurso de Saída: Nome do recurso de saída, que está associado ao evento passivo.
- Valor Recurso Saída: Valor do recurso de saída.
- Operador Lógico: Será apresentado uma DropDownList com os operadores lógicos.
- Nome do Dispositivo: Será apresentado uma DropDownList com todos os nomes de Dispositivos associados a conta em uso.
- Nome do Recurso de Entrada: Será apresentado uma DropDownList com todos os nomes dos Recursos associados ao Dispositivo selecionado acima.
- Tempo Evento Ativo: Tempo que o evento ficará ativo.
- Valor Inicial Evento: Valor que será armazenado no Feed do recurso associado, por ocasião do início da execução do evento.
- Valor Final Evento: Valor que será armazenado no Feed do recurso associado, por ocasião do término da execução do evento.
- Situação Evento: Evento Ativado ou Desativado, no modo Desativado o evento não será executado.
- Ativa Evento uma Única Vez: Opção ativada o evento será ativado apenas uma vez.

.. important:: Evento passivo será executado quando o **Valor do Recurso de Saída** associado com o **Operador lógico** for verdadeiro.

.. _Mapa:

Mapa
~~~~

.. image:: ../imagem/mapa.png
    :align: center

Através da opção *Mapa* poderá ser visualizado todos os dispositivos cadastrados na conta em uso.

O marcador estará associado ao ícone selecionado, por ocasião do cadastro deste.

.. note:: Marcadores

  - Marcador em *Vermelho* estará representando dispositivo Desativado,
  - Marcador em *Verde* estará representando dispositivo Ativado.


.. _Log Dispositivo:

Log Dispositivo
~~~~~~~~~~~~~~~

Responsável por exibir Log de reset do dispositivo.

.. image:: ../imagem/log-device.png
    :align: center

.. note:: Mensagens de logs

  - Power reboot,
  - Hardware WDT reset,
  - Fatal exception,
  - Software watchdog reset,
  - Software reset,
  - Deep-sleep,
  - Hardware reset.


.. _Syscall:

Syscall
~~~~~~~

Responsável por cadastrar chamadas de Syscall, que será executado pelo Dispositivo.

.. image:: ../imagem/dashboard-syscall.png
    :align: center

.. note:: Atualmente o sistema IOT possui 2 chamadas de sistema (Syscall)

  - Reiniciar: Executa reset no Dispositivo ,
  - Reiniciar - Modo Configuração Wifi: Limpa configurações Wifi (SSID, PASSWD).
