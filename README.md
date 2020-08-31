The following set of scripts were written under the project, which's agenda was to generate an automated method to maintain the current software stack. 

The independent scripts in the following project are -


1.pythonSearcher.py

INFO: This script looks up the software's name on the internet, scrapes the important data, and then the scraped data is converted into a .metadata.json which is stored inside the software's folder inside the stack.
USAGE: pythonSearcher.py is a Python Class. To use it, the user is required to import it like a Python Package. 

2.json_combine.py

INFO: This script combines all the JSONs found in the software stack folders into a single combined_json.json
USAGE: python json_combine.py <PATH_TO_SOFT_STACK> <PATH_TO_STORE_JSON> ( Can be called through CLI )

3.install_script_verify.py

INFO: It verifies the installation bash scripts by going through their mirrors and verifying them. It then generates a logfile based on the data collected.
USAGE: python install_script_verify.py <PATH_TO_SCRIPT_NAME> ( Can be called through CLI )


The driver files run the scripts. The driver files are -

1.fullstack_generator.py

INFO: This script looks through the defined directory, and then generates metadata jsons for all the software folders found.
USAGE: python fullstack_generator.py <PATH> ( Can be called through CLI )

2.metadata_helper.py

INFO: Driver script to run pythonSearcher.py for a specific software. 
USAGE: python metadata_helper.py <SOFTWARE_NAME> <PATH_TO_SOFTSTACK> ( Can be called through CLI )