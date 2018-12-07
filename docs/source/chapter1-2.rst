chapter 2: Teleporting with Variables
=========================================


2.1 What Is a Program?
--------------------------

A program is a set of instructions that makes your computer do a specific
task or tasks


2.2 Storing Data with Variables
---------------------------------
이 장에서 배우게 될 중요한 내용은 변수이다.
variable 로 표현되며 여러가지 내용물을 채울 수 있는 모양이 변형되는 그릇이라고 생각하면 된다.

pickaxes = 12 할당해 보자.

bread=145  할당해 보자.


.. code-block:: python

    from mcpi.minecraft import Minecraft
    mc = Minecraft.create()
    import time

    pickaxes = 12

    bread=145

    time.sleep(2)
    mc.postToChat(pickaxes)

    time.sleep(2)
    mc.postToChat(bread)



다음은 입력이 안된다.

pickaxes = 12 iron = 30 cobblestone = 25
A syntax error is Python’s way of telling you it doesn’t understand


Syntax Rules for Variables
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

다음은 변수로 쓸수 없는 규칙이다.


.. sourcecode:: pycon

    • Don’t include symbols in your variable names, except for underscores (_),
    or you’ll get a syntax error.
    • Don’t start a variable name with a number, as in 9bread. Using numbers
    elsewhere in a variable name is fine, as in bread9.
    • You don’t need to add spaces on either side of the equal sign: your program
    will run fine without them. But they do make the code easier to
    read, so it’s a good idea to add them.



Although the value of a variable is stored, it is not saved. The value of a variable
is stored in the computer’s temporary memory, meaning that when the computer is
switched off or the program stops running, the value of the variable is no longer
stored. Try closing IDLE and then opening it again. When you try to get the value
of bread, what happens?

Changing the Values of Variables
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

변수는 변경이 가능하다.


.. code-block:: python

    from mcpi.minecraft import Minecraft
    mc = Minecraft.create()
    import time

    pickaxes = 12

    bread=145

    time.sleep(2)
    mc.postToChat(pickaxes)


    time.sleep(2)
    mc.postToChat(bread)


    time.sleep(2)

    pickaxes = 30
    bread=20

    time.sleep(2)
    mc.postToChat(pickaxes)


    time.sleep(2)
    mc.postToChat(bread)

Integers
~~~~~~~~~~~~~~~~~

정수를 의미한다.
다음에서 x,y,z 변수값을 넣어 보자.
라즈베리 파이에서 평면은
X : -127 ~ 127
Y : -127 ~ 127
Z : -127 ~ 127
공간 안에서만 입력할 수 있다.
프로그램상에서는 다양한 값을 넣을 수 있다.


.. code-block:: python


    from mcpi.minecraft import Minecraft
    import mcpi.block as block
    import time

    mc = Minecraft.create()


    #Set x, y, and z variables to represent coordinates

    x = 60
    y = 1
    z = 113
    """
    x = 0
    y = 0
    z = 0
    """
    #Change the player's position
    # mc.player.setTilePos(x, y, z)
    mc.player.setTilePos(x, y, z)

    time.sleep(5)

    mc.postToChat("this is sean notebook")



Floats
~~~~~~~~~~~~~~~~~

정수를 포함한 소수까지 확장은 넓은 변수이다.
소숫점 이하 정확한 지점까지 이동해 보자.

.. code-block:: python


    #Connect to Minecraft
    from mcpi.minecraft import Minecraft
    mc = Minecraft.create()

    #Set x, y, and z variables to represent coordinates
    x = 63.5
    y = 1.0
    z = 113.5

    #Change the player's position
    mc.player.setPos(x, y, z)



2.3 Slowing Down Teleportation Using the time Module
------------------------------------------------------

player를 좀 느리게 처리를 하려면 다음 모듈을 쓰면 된다.

.. code-block:: python


    import time

    time.sleep(초)






2.4 Debugging
-------------------
Everyone makes mistakes

다음을 실행해 보자.

.. code-block:: python

    from mcpi.minecraft import Minecraft
    mc = Minecraft.create()

    #Set x, y, and z variables to represent coordinates
    #x = 63.5
    y = 1.0
    z = 113.5

    #Change the player's position
    mc.player.setPos(x, y, z)


버그를 수정해 보자.
버그 1

.. code-block:: python


    from mcpi.minceraft inport Minecraft
    # mc = Minecraft.create()

    x = 10
      y = 11
    z = 12


버그를 수정해 보자.
버그 2

.. code-block:: python

    from mcpi.minecraft import Minecraft
    mc = Minecraft.create()

    x = 120
    y = 4
    z = -12

    # mc.player.setPos(x, z, y)
    mc.player.setTilePos(x, y, z)




2.5 What You Learned
-----------------------

player position


variables
- integers
- floats

setPos()
setTilePos()



