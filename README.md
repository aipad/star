# Star

Not documented at all.

To compile:
1. Make sure you have MacPorts installed, and python26, plus fuse if you want to compile dsc.c (which isn't necessary).
2. Copy stuff into bs/, e.g.
bs/iPhone2,1_4.0.1
bs/iPhone2,1_4.0.1/cache
bs/iPhone2,1_4.0.1/kern
bs/iPhone2,1_4.0.1/launchd

where cache is /System/Library/Caches/com.apple.dyld/dyld_shared_cache_armv[67], launchd is /sbin/launchd, and kern is the decrypted kernel.  Note that you can get 'kern' on platforms like the iPhone 4 where we don't have keys yet by using /dev/kmem and bs/unload.py, but there's a chance the kernel already overwrote __LINKEDIT with crap.

3. config/config.py iPhone2,1_4.0.1
4. make
5. fix the places where you need to copy headers from OS X and I fail at documentation, goto 4
6. look at cff/out.pdf
