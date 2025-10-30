

OS := $(shell uname)

ifeq ($(OS), Linux)
	BLENDER=../../blender-4.5.2-linux-x64/blender
else
	BLENDER=/Applications/Blender.app/Contents/MacOS/Blender
endif

all : \
	../dist/spheres.pnct \
	../dist/spheres.scene \

../dist/spheres.scene : spheres.blend export-scene.py
	$(BLENDER) --background --python export-scene.py -- 'spheres.blend' '$@'

../dist/spheres.pnct : spheres.blend export-meshes.py
	$(BLENDER) --background --python export-meshes.py -- 'spheres.blend' '$@'

#../dist/pool.scene : pool.blend export-scene.py
#	$(BLENDER) --background --python export-scene.py -- 'pool.blend:Table 1' '$@'

#hexapod.pnct : hexapod.blend export-meshes.py
#	$(BLENDER) --background --python export-meshes.py -- hexapod.blend:Main '$@'
#hexapod.scene : hexapod.blend export-scene.py
#	$(BLENDER) --background --python export-scene.py -- hexapod.blend:Main '$@'
