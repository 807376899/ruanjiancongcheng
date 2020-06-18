# 虚拟机技术与软件综述报告
## 摘要
虚拟化是一种用于创建虚拟环境以识别和隔离用户数据的进程。它允许用户通过创建操作系统、服务器或网络资源的虚拟版本，在一台计算机上同时运行多个操作系统。随着IT产业的日益发展，虚拟机技术为计算机的发展和学习提供了一个更为便捷的平台，同时也在促进着云计算等新兴技术的不断壮大，本文从发展与应用、先进代表、经典开发框架、对软件工程的推动等方面对虚拟机技术进行了介绍。
## Abstract
Virtualization is a process used to create a virtual environment to identify and isolate user data.It allows users to run multiple operating systems simultaneously on a single computer by creating virtual versions of operating systems, servers, or network resources.With the development of IT industry, the virtual machine technology to the development of the computer and study provides a more convenient platform, but also in promoting the emerging technologies such as cloud computing has grown, this article from the development and application, advanced representative and classic development framework, push about software engineering and other aspects of the virtual machine technology are introduced.
## 简介
虚拟化是一种用于创建虚拟环境以识别和隔离用户数据的进程。它允许用户通过创建操作系统、服务器或网络资源的虚拟版本，在一台计算机上同时运行多个操作系统。虚拟机技术是虚拟化技术的一种，是将计算机的各种实体资源，如服务器、网络、内存及存储等，予以抽象、转换后呈现出来，打破实体结构间的不可切割的障碍，使用户可以比原本的组态更好的方式来应用这些资源。这些资源的新虚拟部分是不受现有资源的架设方式，地域或物理组态所限制。它允许用户通过创建操作系统、服务器或网络资源的虚拟版本，在一台计算机上同时运行多个操作系统。虚拟化允许在一台机器上运行多个服务器，同时将服务器彼此隔离。随着IT产业的日益发展，虚拟机技术为计算机的发展和学习提供了一个更为便捷的平台，同时也在促进着云计算等新兴技术的不断壮大，本文从虚拟机技术的分类、发展与应用、虚拟机技术的先进代表、经典开发框架以及虚拟机技术对软件工程的推动等方面对虚拟机技术进行了介绍。

## 虚拟机技术概述
### 虚拟机技术概览
虚拟机（Virtual Machine）指通过软件模拟的具有完整硬件系统功能的、运行在一个完全隔离环境中的完整计算机系统。在实体计算机中能够完成的工作在虚拟机中都能够实现。在计算机中创建虚拟机时，需要将实体机的部分硬盘和内存容量作为虚拟机的硬盘和内存容量。每个虚拟机都有独立的CMOS、硬盘和操作系统，可以像使用实体机一样对虚拟机进行操作。
虚拟机技术是虚拟化技术的一种，虚拟化是一种用于创建虚拟环境的过程，用于识别和隔离用户的数据。是将计算机的各种实体资源，如服务器、网络、内存及存储等，予以抽象、转换后呈现出来，打破实体结构间的不可切割的障碍，使用户可以比原本的组态更好的方式来应用这些资源。这些资源的新虚拟部分是不受现有资源的架设方式，地域或物理组态所限制。它允许用户通过创建操作系统、服务器或网络资源的虚拟版本，在一台计算机上同时运行多个操作系统。虚拟化允许在一台机器上运行多个服务器，同时将服务器彼此隔离，因为它们运行在不同的虚拟机上。[1]
### 虚拟机技术分类
目前，虚拟化技术主要流行的技术分类可以分为平台虚拟化、桌面虚拟化和应用虚拟化等类别。
* 平台虚拟化(Platform Virtualization)：
平台虚拟化又称硬件虚拟化，主要包括CPU、内存、磁盘和I/O 等部件的虚拟化。它是在硬件和传统的操作系统之间插入一个超级管理程序，操作系统不再直接运行在计算机硬件上，而是在Hypervisor 之上。操作系统称为客户机，Hypervisor 系统称为主机。客户机可以完全实现用户在传统物理机上的各种应用需求，实现对各种资源的访问和操作。
* 桌面虚拟化(Desktop Virtualization)：桌面虚拟化是相对传统的计算机桌面而言的，用户通过网络访问一台可集中控制的服务器，也可以由服务器将所需要的信息推送给用户所在设备。
* 应用虚拟化（Application Virtualization）：从技术实现角度来说，应用虚拟化与硬件虚拟化有着非常明显的差异，应用虚拟化不是将底层的硬件通过各种虚拟化技术模拟出一台或多台虚拟机，而是将应用程序进行重新封装，在运行时，将所有的文件和注册表操作重定向到一个特定的文件，从而满足应用程序对底层硬件的访问需要，使应用程序直接对硬件进行操作。

### 虚拟机技术的发展
* 1959年6月，牛津大学的计算机教授Christopher Strachey在《大型高速计算机中的时间共享》（Time Sharing in Large Fast Computer）[2]中首次提出了“虚拟化”的基本概念，还论述了什么是虚拟化技术，从此拉开了虚拟化发展的帷幕。
* 1960中期，IBM 在Thomas J. Watson Research Center (NY)进行M44/44X 计算机研究项目。实现了多个具有突破性的虚拟化概念，包括部分硬件共享、时间共享、内存分页以及实现了虚拟内存管理的VMM。通过这些虚拟化技术，应用程序可以运行在这些虚拟的内存之中，实现了在同一台主机上模拟出多个 7044 系统（44X）。M44/44X项目首次使用了VM（Virtual Machine）和VMM（Virtual Machine Monitor）一词，被认为是世界上第一个支持虚拟机的系统。
* 1999年，VMware公司率先推出针对x86平台推出了可以流畅运行的商业虚拟化软件VMaware Workstation。
* 2000年，FreeBSD jail，真正意义上的第一个功能完整的操作系统虚拟化技术。利用这个技术，FreeBSD的系统管理者，可以创造出几个小型的软件系统，这些软件系统被称为jails。
* 从2008 年起，虚拟化技术己经进入很多应用领域，且己被大众所接受。虚拟化的目的就是要对IT基础设施进行简化，通过处理器虚拟化、内存虚拟化、I/0 虚拟化和网虚拟化等技术，提高IT 资源的利用率和灵活性，降低IT 运维成本和管理成本。[3][4][5]
* 如今，虚拟机技术与云计算相结合，虚拟机资源作为云计算环境中的主要资源，数据中心的各种硬件资源通过使用虚拟化技术形成虚拟资源池，系统动态部署虚拟机，用户透明使用。[6][7][8]

## 虚拟机技术在工业和学术界的先进代表
VMware虚拟化技术是由美国VMware软件公司研发的资源管理技术，主要安装于计算机硬件以及计算机主机的操控系统中。VMware虚拟化技术的应用形式极其简单，仅需通过软件包的形式就能完成安装工作。同时，VMware虚拟化技术在安装过程中还能根据安装对象的不同形式进行安装，从而实现同时操作多个不同形式机器的目的，使各机器之间达到资源共享。将VMware虚拟化技术应用至计算机中，能够使原本属于计算机中的操作系统独立出来，以此运行更为严谨的监督程序。VMware虚拟化技术在实际应用过程中，不仅能够保障机器本身的平稳运行，还能提高数据处理能力。[9]
1998年1月，Stanford大学的Mendel Rosenblum教授带领他的学生Edouard Bugnion和Scott Devine及对虚拟机技术多年的研究成果创立了VMware公司，主要研究在工业领域应用的大型主机级的虚拟技术计算机，并于1999年首次将虚拟化技术引入到x86计算平台上，VMware虚拟化将操作系统从运行它的底层硬件中抽离出来，并为操作系统及其应用程序提供标准化的虚拟硬件，从而使多台虚拟机能够在一台或多台共享处理器上同时独立运行[10]。尔后于2001年推出了面向服务器市场的VMware GSX Server和VMware ESX Server。今天VMware是虚拟机市场上的领航者，其首先提出并采用的气球驱动程序(balloon driver)，影子页表(shadow page table)，虚拟设备驱动程序(Virtual Driver)等均已被后来的其它虚拟机如Xen采用。
在所有通过虚拟化技术对IT环境进行优化和管理的软件中，VMware虚拟化技术得到了最为广泛应用，从桌面环境到数据中心均有涉及。
VMware作为服务器虚拟化的领跑者，开发了桌面虚拟化产品View。其后台架构在成熟且强大的服务器虚拟化平台vSphere 上，远程访问使用了自有的PCOIP 协议，提供了与真实PC 机相媲美的用户体验。
VMware View 桌面虚拟化架构主要由四部分组件构成：VMware vSphere、View Connection Server、View Composer 和View Client。[11]
VMware View 后台构建于vSphere 之上，vSphere平台由多台安装ESXi 操作系统的物理主机组成，每台ESXi 主机上可以承载几十到上百台虚拟机。
View Connection Server 是虚拟桌面访问管理器，管理客户端与虚拟桌面的连接，同时提供View Administrator 服务，允许管理员进行配置设置、管理虚拟桌面和设置桌面的权限以及分配应用程序。
View Composer 是创建链接克隆（Linked Clone）虚拟桌面的组件，可以安装在vCenter Server 实例上或单独服务器上。Composer可以从指定的父虚拟机创建链接克隆池，链接克隆与父虚拟机共享一个基础映像，因此，存储需求明显减少，而且还可极大降低桌面维护成本。
View Client 是View 客户端程序，将该程序安装在瘦客户机上，使View Client 与View Connection Server 进行通讯，实现用户与虚拟桌面
的连接[12]。
View的客户端可以是PC、笔记本电脑、上网本、瘦客户机、平板电脑或手机等智能设备，这些终端设备需要安装客户端软件View Client。

## 虚拟机技术推进软件工程
### 虚拟机技术推进软件开发与编码
软件进入实际开发阶段，程序员开始写代码的时候离不开编程语言，而java语言就是当前主流的编程语言之一。Java语言的一个非常重要的特点就是与平台的无关性。而使用Java虚拟机（Java Virtual Machine 简称JVM）是实现这一特点的关键。
Java虚拟机是运行所有Java程序的抽象计算机，是Java语言的运行环境，它包括一套字节码指令集、一组寄存器、一个栈、一个垃圾回收堆和一个存储方法域。[13]一旦一个Java虚拟机在给定的平台上运行，任何Java程序（编译之后的程序，称作字节码）都能在这个平台上运行。Java虚拟机（JVM）可以以一次一条指令的方式来解释字节码（把它映射到实际的处理器指令），或者字节码也可以由实际处理器中称作just-in-time的编译器进行进一步的编译。
一般的高级语言如果要在不同的平台上运行，至少需要编译成不同的目标代码。而引入Java语言虚拟机后，Java语言在不同平台上运行时不需要重新编译。Java语言使用模式Java虚拟机屏蔽了与具体平台相关的信息，使得Java语言编译程序只需生成在Java虚拟机上运行的目标代码（字节码），就可以在多种平台上不加修改地运行。
这打破了对开发平台的限制，大大提高了软件开发的效率。

### 虚拟机技术推进软件测试
测试团队经常需要搭建不同的测试环境。使用物理机来搭建这些测试环境，往往需要大量的成本，而且维护这些物理机也是很费时的。而虚拟机可以在宿主计算机中虚拟出一个或多个操作系统。可以在虚拟出的操作系统中进行测试环境的搭建。使用虚拟机则可以节省这些硬件成本，而且可以节省大量测试机器的安装时间与测试环境恢复时间。虚拟机对软件测试促进主要有以下几点：
1. 利用虚拟机可以快速搭建环境
使用虚拟机搭建完测试环境后可以共享给其他的小组成员，这样可以节省测试团队搭建测试环境的时间。
2. 虚拟机快照的应用
快照重现难以重现的BUG：对测试人员来讲，经常会有一些难以重现的BUG。虚拟机的另一个好处就是可以对于难以重现的BUG，可以用快照的方式保存下BUG重现时的环境，开发人员只要打开该快照就可以快速的观看到这个BUG。这对于重现非与外界网络直接交互的BUG非常有效。
快照搭建杀毒环境：使用不同的杀毒软件对企业产品的病毒的查杀，但是在一个系统中同时安装多个杀毒软件，会导致各种杀毒软件的相互冲突。使用快照来安装各杀毒软件，可以解决杀毒软件间冲突的问题。
快照快速切换测试环境：在物理测试机中恢复到测试初始环境总是一件非常费力的事情。使用快照不但可以快速的恢复到测试的初始环境，还可以快速的切换其他几种测试环境。
3. 利用虚拟机搭建测试集群
利用虚拟机，我们可以在一台计算机中虚拟出一个或多个操作系统，这样测试人员就可以在一台台式机或者笔记本上搭建测试集群。大大节省了成本。

## 虚拟机技术在中国的发展和成长
### 虚拟机技术的应用
* 教学中的应用：将VMware虚拟化技术应用至教学领域中，能够通过计算机的实际配置情况搭建起多媒体教室，为学校构建起虚拟网络教学模式。通过此方式，不仅能够极大程度上缓解学校实验室紧张这一现状，还能起到降低教学成本、提高教学效率的多种作用。同时，VMware虚拟化技术在教学领域的运用，还将彻底改变学校教学方式，为我国数字化校园的建设起到促进作用。
* 医疗领域的应用：随着互联网+战略的深入推进，医疗领域基本已将互联网平台替代传统人工记录方式，对病人信息及病历进行管理。将VMware虚拟化技术运用至医疗领域中，能够减轻医院在虚拟机以及数据服务器方面的投入，进一步优化医疗资源网络配置。同时，将VMware虚拟化技术运用至医院业务系统中，能够实现医院各业务部门之间不同信息的统一化管理，为医院各系统的运行提供保障。
* 在传媒云领域的应用：传媒云是一种以计算机模型为主的传媒行业新型运营模式，具备共享内容生产云、信息服务云、产品交易云等丰富内容，是当前信息服务领域不可或缺的新型技术。将VMware的虚拟化技术运用至传媒云领域中，搭建起以传媒云为主的原型，以此实现传媒系统桌面在各常用终端中的发布，如台式计算机、平板电脑、手机等，从而达到传媒数据在线存储以及迁移的目的。如此一来，不仅能够提高传媒业务的资源整合及数据集中能力，还能对传媒云的多样化终端访问起到支持作用。VMware虚拟化技术在传媒云领域的具体技术路线
* 在桌面系统的应用：虚拟桌面实则就是一种基于虚拟化技术的桌面。也就是说，将VMware的虚拟化技术运用至桌面系统中，能够将计算中的桌面进行虚拟化，扩大桌面系统在时间以及地点上的空间。同时，将VMware的虚拟化技术运用至桌面系统中，还能进一步实现数字资源的集中化管理，以统一化方式对各类资源进行配置，以此提高信息数据的安全性。基于VMware的虚拟化技术的桌面系统。

### 典型产品
VMLite是全球首款中国人自己设计的高速虚拟机，VMLite发布的短短几周内已经吸引了全球上万名虚拟机玩家注册下载并使用VMLite软件。
VMLite是一个虚拟机软件，已经包括VMLite XP Mode、VMLite Workstation、MyOldPCs、VMLite VirtualApps Studio、VMLite VirtualApps Player、VBoot六大产品，非常全面。其中VMLite XP模式与微软推出的Windows XP模式几乎一模一样，但是却不要求你的CPU非得支持虚拟化才能运行。VMLite允许你直接使用从微软网站上下载下来的Windows XP模式安装文件，来建立Windows XP虚拟机。VMLite XP模式配置完成后，在Windows 7的开始菜单中也会出现虚拟机中安装的软件的快捷方式;在虚拟机中运行的程序，可以无缝的在Windows 7桌面上显示，看起来就跟在本机中运行一样。

## 虚拟机技术应用到软件产品以及软件产品范例
### VMware Workstation
VMware是EMC公司旗下独立的软件公司，使用Vmware，可以同时运行Linux各种发行版、Dos、Windows各种版本，Unix等，甚至可以在同一台计算机上安装多个Linux发行版、多个Windows版本。
### Parallels Desktop
Parallels Desktop是适用于Mac OS平台上的虚拟机解决方案。无需重启即可在同时一台Mac电脑上随时访问Windows和Mac两个系统上的众多应用程序。与VMware最大的区别在于Parallels Desktop无需重启，两个系统同时运行。两系统间可以实现文件互传，素材共用。
融合模式(Coherence)支持不显示Windows但是仍使用其应用程序，或者在Mac上保留熟悉的Windows背景与开始菜单。两种同时运行Windows与Mac应用程序的方式都不会对性能产生任何影响。
### Virtual PC
Virtual PC是微软公司(Microsoft)收购过来的，最早不是微软开发的。Virtual PC可以允许你在一个工作站上同时运行多个PC操作系统，当你转向一个新OS时，可以为你运行传统应用提供一个安全的环境以保持兼容性，它可以保存重新配置的时间，使得你的支持，开发，培训工作可以更加有效。
Virtual PC在使用PowerPC处理器的Mac OS X版本上，其模拟机“使用”Intel Pentium 4处理器及440BX系列的主板;而在Windows版本上，会使用电脑本身的处理器。具有兼容性小、占用内存小、对网络的支持好等优点。
### Oracle VM VirtualBox
Oracle VM VirtualBox是由Sun Microsystems公司出品的软件(Sun Microsystems于2010年被Oracle收购)，原由德国innotek公司开发。2008年2月12日，Sun Microsystems宣布将以购买股票的方式收购德国Innotek软件公司，新版不再叫做Innotek VirtualBox，而改叫Sun xVM VirtualBox。2010年1月21日，欧盟终于同意Oracle收购Sun，VirtualBox再次改名变成Oracle VM VirtualBox。VirtualBox是开源软件。
VirtualBox 3.2.0支持的操作系统包括:Debian，Fedora，Linux，Mac OS (Intel)，Mandriva，OpenSolaris，PCLiunxOS，Red Hat，SUSE Linux，Solaris 10，Ubuntu，Windows，Xandros，openSUSE等。
Oracle VM VirtualBox支持的客户端操作系统包括:从3.1到Vista的所有版本的Windows、Linux 2.2、2.4和2.6内核、Solaris x86、OS/2、、OpenBSD、Netware、FreeBSD和DOS。在2007年1月，InnoTek以GNU General Public License (GPL)释出VirtualBox，并提供二进位版本及开放源码版本的代码。
VirtualBox的界面风格简洁，操作简便，系统启动时间也很短，对于初学者来说十分容易上手。[14]
### VMLite
VMLite是全球首款中国人自己设计的不运行远程程序的高速虚拟机。作为世界上运行速度最快的虚拟机)，VMLite拥有2TB超大磁盘容量，同时支持32位和64位系统，支持多个虚拟CPU同时运行。不仅如此，对硬件安装没有任何要求，就是对你的计算机配置没有任何要求，比如不需要兼容VT-x或者AMD-V。

## 虚拟机技术的应用开发框架概述
VMware在原来的VMware基础上推出的VMware vSphere被称为业界首款云计算操作系统。VMware vSphere主要包括两部分：一是虚拟化VMM管理器部分，VMware ESX 4；二是用于整合和管理的VMM的VMware vCenter。[15]其架构如下图所示。
![输入图片说明](https://images.gitee.com/uploads/images/2020/0609/142829_923173cc_7609513.png "屏幕截图.png")
 
虚拟化从结构上可以分为寄居架构和裸金属架构（Bare Metal)。寄居架构指的是在操作系统的层面之上进行虚拟机实现，VMware开发的VMware Workstation系列就属于寄居架构。裸金属架构是在计算机硬件上直接进行虚拟化，是架设在计算机硬件和操作系统之间的虚拟化。通过裸金属架构的虚拟化，计算机硬件直接被切割成若干个虚拟机，然后在这些虚拟机上再进行各自的系统和应用程序的安装，这样一来，虚拟机的底层是虚拟出来CPU、内存等计算机硬件资源，而不是操作系统，虚拟机之间完全独立。
vSphere的底层就是VMware推出的虚拟机EXS Server。通过EXS虚拟化数据中心服务器，将数据中心转换为云计算基础架构，满足IT组织利用内部和外部资源、低成本地提供云服务的能力。EXS Server属于裸金属架构的虚拟机。EXS Server直接安装在服务器租用硬件上，在硬件和操作系统之间插入了一个稳固的虚拟化层。EXS Server将一个物理服务器划分为多个安全、可移植的虚拟机，这些虚拟机在同一物理服务器上运行。每个虚拟机都呈现为一个完整的系统（具有处理器、内存、网络、存储器和BIOS），因此Windows、Linux、Solaris和NETWare操作系统和软件应用程序都可以在虚拟机中运行，无需进行任何修改。
EXS Server是向IT环境提供基于虚拟化的分布式服务的基础。SEX最新的版本是EXS Server4,和之前EXS Server3.5/3相比，在功能和特性上有很多更新和扩展，其中最大的区别在于EXS Server4只支持64bit运行模式，只能安装在支持64位计算的X86物理服务器上。除了EXS，VMware还推出了精简版的ESXI，EXSI与ESX的最大区别在于ESXI去除了Server Console。

## 参考文献
1.	G. Sunitha Rekha. A Study On Virtualization And Virtual Machines, International Journal of Engineering Science Invention [J], 2018, vol.7.
2.	C. Strachey. Time sharing in large, fast computers, Proceedings of the IFIP Congress [C], 1959, pp.336-341
3.	丁佐杉, 满喜东, 许新房. 服务器虚拟化部署研究与分析[J]. 计算机光盘软件与应用,2012,5:43-44.
4.	张超.VMware 虚拟化服务器的构建方法与展望[J]. 通信技术,2010,43(9):88-91.
5.	韩寓. 服务器虚拟化技术研究与分析[J]. 电脑知识与技术,2011,7(7):1654-1655.
6.	袁爱平. 云计算环境下虚拟机部署策略研究[J]. 计算机与数字工程, 2018, 第46卷(8):1598-1602.
7.	Kamiyama N . Virtual Machine Trading in Public Clouds[J]. IEEE Transactions on Network and Service Management, 2019, PP(99):1-1.
8.	Lopez-Pires F , Baran B . Virtual Machine Placement Literature Review[J]. computer science, 2015.
9.	尹超,张雷．试析VMware虚拟化技术的运用[J]．数字化用户,2018,024(012):59.
10.	张进铎,曹士炳,张卫华,等.VMware虚拟化技术及其应用的综合剖析[J].信息技术与信息化,2014(1):101-106.
11.	汤旻辰. VMware虚拟化技术及其应用的综合分析[J]. 中国新通信, 2017(9).
12.	周骅.VMware技术实现机房设备虚拟化管理[J]. 现代机械,2012,5:88-91.
13.	Liang S , Bracha G . Dynamic class loading in the Java virtual machine[J]. Acm Sigplan Notices, 1998, 33(10):36-44.
14.	罗晓慧. 虚拟机技术的应用[J]. 电子世界, 2019, 000(009):101.
15.	Marië, AndrÉ N . review: VMware vSphere and virtual infrastructure security: securing the virtual environment[J]. Computing Reviews, 2010, 6(11):952-953.
