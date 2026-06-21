
Send request
response = requests.get(url)

# Check status
if response.status_code == 200:
    soup = BeautifulSoup(response.text, "html.parser")

    # Extract all headings
    headings = soup.find_all("h1")

    print("Headings found:")
    for heading in headings:
        print(heading.text.strip())
else:
    print("Failed to retrieve webpage")
Python
