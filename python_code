import csv
import requests

# API credentials
api_url = 'https://sandbox.piano.io/api/v3'
application_id = 'o1sRRZSLlw'
api_token = 'xeYjNEhmutkgkqCZyhBn6DErVntAKDx30FqFOS6D'

# Create a dictionary to store user data from File B
user_data_dict = {}
with open('file_b.csv', mode='r') as file_b_csv:
    reader = csv.DictReader(file_b_csv)
    for row in reader:
        user_data_dict[row['user_id']] = {'first_name': row['first_name'], 'last_name': row['last_name']}

# Create a list to store the merged data
merged_data = []

# Open File A and process its data
with open('file_a.csv', mode='r') as file_a_csv:
    reader = csv.DictReader(file_a_csv)
    for row in reader:
        email = row['email']
        
        # Make an API request to fetch user ID
        response = requests.get(
            f'{api_url}/user?aid={application_id}&email={email}',
            headers={'Authorization': f'Bearer {api_token}'}
        )
        
        if response.status_code == 200:
            data = response.json()
            user_id = data['id']
            first_name = user_data_dict.get(user_id, {}).get('first_name', '')
            last_name = user_data_dict.get(user_id, {}).get('last_name', '')
        else:
            # Use the provided user_id from File A
            user_id = row['user_id']
            first_name = ''
            last_name = ''
        
        merged_data.append({'user_id': user_id, 'email': email, 'first_name': first_name, 'last_name': last_name})

# Create and write the merged data to a new CSV file
with open('merged_data.csv', mode='w', newline='') as merged_csv:
    fieldnames = ['user_id', 'email', 'first_name', 'last_name']
    writer = csv.DictWriter(merged_csv, fieldnames=fieldnames)
    
    writer.writeheader()
    for row in merged_data:
        writer.writerow(row)

