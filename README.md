# Springinternals

#### Before going  to know about spring internals we need to know some basic knowledge about spring
#### 1. Maven : Parent Project - Child Project
#### 2. Starter class | Main Class | BootStrap class
#### 3. Conditional Process

#### ++++++++++++++++++++++++++++++++++++++++++++++++
#### 1. maven :ParentProject - ChildProject
#### =>Create One Maven project using type : pom
#### =>provide possible dependencies using tag
#### =>provide possible dependencies(JARS)
#### =>create one maven project using type : jar/war ( Child Project)
#### => open pom.xml (child project) and add tag parent>
#### =>Inside this tag provide parenr project groupId,artifactId,version
![Dependencies](https://github.com/rammolankula/Springinternals/assets/53596726/698607ed-7fef-43ea-8817-bf752ff66df9)
#### =>Then read parent dependencies using dependency tag by providing only groupId,artifactId version is taken care by parent project
  
#### ============================================================
#### 2. starter class | Main class | BootStrap Class


#### =>Spring Application (done by programmer)
####  a.base-package (ComponentScanning)
####  b.xml/java/Annotation configurations
####  bean
#### @Configuration
#### @Component
#### c.Loading properties files
####  @PropertySource
#### Environment
####  @Value
####  d. Dependency Injection/Life Cycle methods...etc
  
  
#### => Spring Boot :(Starter Class)
####   @SpringBootApplication = Component Scanning(Starter class package)
####                            +Component class + Configuration
#### +Enable AutoConfiguration
#### +Application.properties/.yml(from classpath)
#### run(): Providing Spring container by doing
#### ->Load Properties data into environment memory
#### ->Read main method parameters (args[]) and system args (-Dkey=val)
#### ->print Banner
#### ->Empty Container (Spring IOC container)
#### ->Link to container- environments,banner,listener...etc
#### ->Calling runners
	
	
#### =============================================================
### Conditional Process
#### @Configuration
#### public class Appconfig {
####  public Datasource ds(){
####  DriverManagerDataSources ds=new DriverManagerDataSources();
####  ds.setDriverClassName("___________");
####  ds.setUrl("_______");
####  ds.setUserName("____");
####  ds.serPassword("__________");
####  return ds;
####  }
#### }

#### SpringAutoConfiguration::
#### =========================
####   SpringAutoConfiguration=
#### starter in class path
#### +properties in_.properties/_.yml
#### +conditional objects
	  
#### class/interface___________________extends/implements JpaRepository<T,Id>
