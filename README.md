# Maven & Dropwizard - steps to start a new application


1. 	New Maven project

2. 	GroupId: topoinventari.com
	ArtifactId: El nom de l'aplicació que ara estem fent (Ex: movies)

3. Add .gitignore in the same level of the rooth project. 

4. In pom.xml add dependencies

5. start the git ( git init )

6. in version control of intelliJ we can make the first commit :D

7. in src/main/java create a new directori with the name of GroupId + ArtifactId

8. add readme.md inside the main directory and the dropwizard configuration "my-app.yaml" into de resources directory

9. Create the classes xxxConfiguration.java and xxxxApplication.java in the com.topoinventari.movies directory

10. new folders ("package"):
	controllers + model + services + util inside movies directory
	assets inside resources directory


# Adding a new controller or service

11# Create the class inside controller directory

12# it beggins with the @Path and the @Produces annotation
	@Path("/api/transactions")
	@Produces(MediaType.APPLICATION_JSON)
	public class TransactionApi {
	...
	}

13# Register it in the Application class inside the run method
	- create new instance
	- environment.jersey().register(xxxxxx);




# How to run the application


To try it from IntelliJ IDEA:

1. Go to _Edit Configurations..._
(drop-down menu you see at the top-right)
and in the `MyApp` configuration write `server src/main/resources/my-app.yaml`
in the `Program arguments` input box. Save with _OK_.
1. Run the `MyApp` configuration (from the top-right green play button).
The server will start in a couple of seconds
(you'll see something like `org.eclipse.jetty.server.Server: Started @3051ms` in the console).

