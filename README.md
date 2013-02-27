htmltemplate2js-plugin
======================

Compile html templates and generates a JS file with all templates as variables

Usage
=====

			<plugin>
				<groupId>com.templating</groupId>
				<artifactId>htmltemplate2js-plugin</artifactId>
				<version>1.3.0</version>
				<executions>
					<execution>
						<phase>process-resources</phase>
						<goals>
							<goal>generate-js</goal>
						</goals>
						<configuration>
							<templates-folder>${basedir}/src/main/tpl</templates-folder>
							<output-file>${basedir}/src/main/webapp/resources/js/compiledTemplates.js</output-file>
							<js-template-map-var>app.templates</js-template-map-var>
							<!--Optional: <remove-comments>true</remove-comments> -->
						</configuration>
					</execution>
				</executions>
			</plugin>
			
			
			<pluginRepositories>
				<pluginRepository>
					<id>thirdparty-releases-GL</id>
					<name>GL Thirdparty Releases</name>
					<url>http://nexus.globallogic.com.ar/content/repositories/thirdparty</url>
				</pluginRepository>
			</pluginRepositories>
			