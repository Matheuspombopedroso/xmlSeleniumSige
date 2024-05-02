# General Description

This project is designed to automate the retrieval of XML files of electronic invoices from the SIGE Cloud system, save processed dates, and manage data with a PostgreSQL database. It utilizes Selenium for web navigation and interaction, along with libraries for data manipulation and database connectivity.

# Environment Setup

1. **Environment Variables**: The `load_environment_variables` function loads environment variables from a `env_vars.txt` file. It is essential that this file is properly configured with all necessary credentials for database connection and SIGE Cloud site authentication.

2. **Dependencies**:
   - selenium
   - pandas
   - sqlalchemy
   - webdriver_manager

   Install the dependencies using pip:
   ```bash
   pip install selenium pandas sqlalchemy webdriver-manager
   ```

### Code Structure

The script is divided into several sections, each responsible for a specific part of the automation process:

1. **Database Connection**: Uses `sqlalchemy` to connect and perform operations on a PostgreSQL database.

2. **Web Automation Functions with Selenium**:
   - `realizar_login()`: Logs into the SIGE Cloud system.
   - `selecionar_intervalo_datas_e_download()`: Selects the date range for downloading XMLs and initiates the download.
   - Additional helper functions may be required depending on the web page interactions.

3. **Data Handling and Logging**:
   - `salvar_datas_csv()`: Saves the processed dates into a CSV file for logging.

### Usage

1. Ensure that all environment variables are set and dependencies are installed before running the script. Run the script directly from the terminal or via a task scheduler for regular automation.

2. Export the script from the notebook file

3. Run the command from the terminal

```bash
python script_name.py
```

### Security Considerations

- Ensure the security of credentials stored in `env_vars.txt`.
- Consider mechanisms to handle exceptions and network errors during web interactions.

### Error Logging

The script includes basic exception handling that will log errors during execution, essential for debugging and maintenance.

### Future Improvements

- Implement best security practices for storing credentials.
- Enhance exception handling to make the script more robust against failures.

---

This documentation outline provides a solid foundation for your project documentation. It is recommended to detail each function with specific usage examples and potential errors to assist other developers or end-users.
