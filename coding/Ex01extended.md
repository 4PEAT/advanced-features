### Additional Requirements

#### 6. **User Profile Management**

- **User Profile:**
  - **Attributes:**
    - User's bio or description.
    - Profile picture URL.
    - List of posts liked by the user.
  - **Behavior:**
    - Allow users to update their bio and profile picture.
    - Allow users to like and unlike posts.

- **Profile Management:**
  - **View and Edit Profile:**
    - Allow users to view and edit their bio and profile picture.
  - **Like and Unlike Posts:**
    - Allow users to like and unlike posts.
    - Keep track of the posts liked by each user.

#### 7. **Notifications**

- **Notification System:**
  - **Attributes:**
    - Notifications for each user.
  - **Behavior:**
    - Notify users when they receive a new follower.
    - Notify users when one of their posts receives a like.

#### 8. **Search Functionality**

- **Search System:**
  - **Behavior:**
    - Allow users to search for other users by username.
    - Allow users to search for posts by content keywords.

### Expanded Console Menu Example

```plaintext
Welcome to the Enhanced Social Media Platform!

Main Menu:
1. Register User
2. Delete User
3. Login
4. Logout
5. Add Post
6. Delete Post
7. List Posts by User
8. Follow User
9. Unfollow User
10. View Profile
11. Edit Profile
12. Like Post
13. Unlike Post
14. View Notifications
15. Search Users
16. Search Posts
17. Exit

Please select an option (1-17):
```

### Example Console Interaction for New Features

#### 10. View Profile
```plaintext
Your Profile:
Username: bob
Bio: Software developer who loves to code.
Profile Picture: http://example.com/pic.jpg
Liked Posts: [103, 105, 110]
Followers: [alice, charlie]
Following: [charlie]

Press Enter to return to the main menu.
```

#### 11. Edit Profile
```plaintext
Please enter your new bio: Enthusiastic coder and tech enthusiast.
Please enter the URL of your new profile picture: http://example.com/newpic.jpg
Profile updated successfully!
```

#### 12. Like Post
```plaintext
Please enter the post ID to like: 104
Post liked successfully!
```

#### 13. Unlike Post
```plaintext
Please enter the post ID to unlike: 104
Post unliked successfully!
```

#### 14. View Notifications
```plaintext
Your Notifications:
- alice started following you.
- Your post with ID 101 received a like from charlie.

Press Enter to return to the main menu.
```

#### 15. Search Users
```plaintext
Please enter the username to search: alice
Search Results:
- alice: Bio - Avid reader and writer.

Press Enter to return to the main menu.
```

#### 16. Search Posts
```plaintext
Please enter the keyword to search in posts: first post
Search Results:
- Post ID: 101, Content: This is my first post!, Author: bob

Press Enter to return to the main menu.
```

### Detailed Workflow for New Features

1. **View Profile:**
   - User selects option 10.
   - The application displays the user's profile information, including bio, profile picture URL, liked posts, followers, and following list.

2. **Edit Profile:**
   - User selects option 11.
   - The application prompts the user to enter a new bio and profile picture URL.
   - The user inputs the details.
   - The application updates the profile and confirms the action.

3. **Like Post:**
   - User selects option 12.
   - The application prompts for the post ID to like.
   - The user inputs the post ID.
   - The application adds the post to the user's liked posts and updates the post's like count, confirming the action.

4. **Unlike Post:**
   - User selects option 13.
   - The application prompts for the post ID to unlike.
   - The user inputs the post ID.
   - The application removes the post from the user's liked posts and updates the post's like count, confirming the action.

5. **View Notifications:**
   - User selects option 14.
   - The application displays the user's notifications, such as new followers and likes on their posts.

6. **Search Users:**
   - User selects option 15.
   - The application prompts for the username to search.
   - The user inputs the username.
   - The application displays the search results, showing users whose usernames match the search term.

7. **Search Posts:**
   - User selects option 16.
   - The application prompts for a keyword to search in posts.
   - The user inputs the keyword.
   - The application displays the search results, showing posts that contain the keyword in their content.

