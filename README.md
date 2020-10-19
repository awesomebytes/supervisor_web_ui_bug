# Reproduce bug with supervisord and big list of programs

```bash
# Need to have supervisor installed: sudo pip install supervisor

# Run supervisor with the 60 entries program
supervisord -n -c supervisor_60.conf
# Access the web ui at http://127.0.0.1:9001 entry 59 will not completely load

# Run supervisor with the 60 long entries program
supervisord -n -c supervisor_long_names_43.conf
# Access the web ui at http://127.0.0.1:9001 entry 48 will not completely load
```