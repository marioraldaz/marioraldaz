# Hi there! Welcome to my GitHub world! 🚀

import json
from dataclasses import dataclass
from typing import List, Dict, Any

@dataclass
class Developer:
    name: str
    profession: str
    interests: List[str]
    current_projects: List[str]
    expertise: List[str]
    social_media: Dict[str, str]

    def __init__(self, name: str, profession: str, interests: List[str], current_projects: List[str], 
                 expertise: List[str], social_media: Dict[str, str]):
        self.name = name
        self.profession = profession
        self.interests = interests
        self.current_projects = current_projects
        self.expertise = expertise
        self.social_media = social_media

    def to_json(self) -> str:
        return json.dumps(self.__dict__, indent=4)

# Create an instance of Developer
dev = Developer(
    name="Your Name",
    profession="Software Engineer",
    interests=["Machine Learning", "Web Development", "Data Science"],
    current_projects=["Project A", "Project B", "Project C"],
    expertise=["Python", "JavaScript", "Django", "React"],
    social_media={"LinkedIn": "linkedin.com/in/yourprofile", "Twitter": "twitter.com/yourhandle"}
)

# Decorate with ASCII art and colorful formatting
print(r"""
   ___              _                   ___           _           
  / __|__ _ ___ __ (_)___ _ _  __ ___  | _ ) ___  ___| |_ ___ _ _ 
 | (_ / _` (_-< '  \| / -_) ' \/ _/ -_) | _ \/ _ \/ _ \  _/ _ \ '_|
  \___\__,_/__/_|_|_|_\___|_||_\__\___| |___/\___/\___/\__\___/_|  

""")

print("\033[1;33;40m")  # Yellow text
print("Hello, fellow GitHubbers! 👋")
print("\033[0;37;40m")  # Reset text color

print("Here's a glimpse into my coding universe:")
print(dev.to_json())

print("\033[1;34;40m")  # Blue text
print("Connect with me on social media:")
for platform, handle in dev.social_media.items():
    print(f"{platform}: {handle}")
print("\033[0;37;40m")  # Reset text color

# Output:
# (Colorful ASCII art and formatted JSON representation of Developer)
