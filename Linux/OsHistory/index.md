# Linux

- **Unix OS** was developed in the late 1960s and early 1970s at AT&T's Bell Labs. The first version was released in **1969** by Ken Thompson, Dennis Ritchie, and others. **Key Features**: Unix introduced many fundamental concepts in operating system design, including multitasking, multiuser capabilities, a hierarchical file system, and a powerful command-line interface.
  
- **GNU** project was started by Richard Stallman in **1983**. The goal was to create a complete free and open-source Unix-like operating system. **Development**: The project produced many tools and utilities that are now integral to the functioning of Unix-like systems, but it did not initially provide a complete operating system, as the GNU kernel (GNU Hurd) was not finished in the early years. The GNU Project developed a wide array of essential command-line utilities and tools needed for a functional operating system, such as bash (the Bourne Again SHell), coreutils (basic file and text manipulation tools), grep, awk, sed, and more. These tools provided the foundational functionalities required to interact with the system. https://www.gnu.org/gnu/linux-and-gnu.html
  
- **POSIX (Portable Operating System Interface)** is a set of standardized operating system interfaces and specifications designed to promote compatibility and interoperability between different Unix-like operating systems. POSIX was developed by the IEEE (Institute of Electrical and Electronics Engineers) in conjunction with ISO and the Open Group. Was created in the late 1980s. The standardization process began in **1988** when the IEEE (Institute of Electrical and Electronics Engineers) formed a working group to develop a standard for Unix-like operating systems.

- **Linux(GNU/Linux)** was created by Linus Torvalds in **1991** as a free and open-source alternative to the Unix operating system. While Linus developed the kernel, the rest of the operating system was built using components from the GNU Project, initiated by Richard Stallman to create free software. This included essential utilities, libraries, and development tools. By the early 1990s, Linux combined with GNU software created a fully functional operating system, often referred to as GNU/Linux.

  Linux has aimed for compliance with POSIX since its early development to ensure compatibility with Unix-like systems, but it has never been fully POSIX-compliant in all aspects.

  **Linux kernel doesn't USE SOURCE CODE of UNIX. But it "clones" concepts and philosophy of UNIX.**

# MacOS

- **Classic Mac OS** (1984–1999) **NOT Unix-like** based on not a traditional kernel, but a monolithic system with key OS functions.
- **XNU kernel released 1996**. XNU kernel is Unix-like, but it is not a traditional Unix kernel. Instead, XNU is a hybrid kernel that combines features of both the Mach microkernel and BSD Unix, with additional Apple-developed components. **USES SOURCE CODE ON UNIX**.
- **Darwin OS released 2000.** A fully functional, open-source, **Unix-based OS** that is based on the XNU kernel and includes key elements like device drivers, and essential system utilities. Darwin is mostly POSIX-compatible, but has never, by itself, been certified as compatible with any version of POSIX.
- **Mac OS X** released 2001 based on unix-like kernel (XNU Kernel). Darwin OS was first introduced as the foundation for Mac OS X.
