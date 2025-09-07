# MEO - Acceptance Test Plan: Introduction

## 1. Introduction

### Project Overview

MEO is an innovative dating application that revolutionizes the online dating experience by prioritizing real-world connections over endless digital conversations. Born from the frustration with conventional dating apps that trap users in cycles of "small talk" and virtual interactions that rarely lead to meaningful encounters, MEO offers a direct path from digital matching to physical meetings.

The application's core philosophy centers on eliminating the prolonged messaging phase that often leads to user fatigue and abandoned connections. Instead of spending hours exchanging messages with uncertain outcomes, MEO facilitates immediate progression to in-person meetings once users mutually express interest.

### Target Audience

MEO targets modern dating app users who:
- Are frustrated with endless messaging on traditional platforms
- Prefer authentic, real-world interactions over virtual conversations
- Value efficiency in their dating process
- Seek genuine connections through face-to-face meetings
- Appreciate safety and verification in online dating

The primary demographic includes young professionals and adults aged 18-45 who are comfortable with mobile technology but desire more meaningful dating experiences.

### Main Functionalities

MEO's distinctive features include:

**Core Matching System**: A sophisticated algorithm that suggests compatible profiles based on comprehensive preference settings including age, location, lifestyle choices, and personal values.

**Card-Based Profiles**: Users create rich, engaging profiles through customizable "cards" containing various content types (text, images, audio messages, music snippets, movie preferences) that provide authentic glimpses into their personalities.

**Direct Date Setup**: After matching, verified users can immediately propose and coordinate real-world meetings, selecting from curated favorite locations and available time slots.

**Identity Verification**: An internal KYC (Know Your Customer) system that verifies user identities through government ID analysis and facial recognition, ensuring safety and authenticity.

**Smart Location Integration**: The app suggests meeting venues based on users' preferred date locations, creating personalized and comfortable meeting experiences.

**Safety-First Approach**: Comprehensive reporting systems, user verification, and safety features that prioritize user security during the transition from digital to physical meetings.

**Subscription & Premium Features**: Advanced matching algorithms, enhanced profile customization options, and priority placement in suggestion queues available through premium subscriptions.

**Targeted Advertising Platform**: Relevant, location-based advertisements for local businesses, restaurants, and entertainment venues that enhance the dating experience while generating revenue.

### Importance of the Acceptance Phase

The acceptance testing phase is critical for MEO's success as it represents the final validation before public release. This phase ensures that:

**Safety and Security**: Given MEO's focus on facilitating real-world meetings, the acceptance phase rigorously tests identity verification systems, reporting mechanisms, and user safety features. Any security vulnerabilities discovered during this phase can be addressed before potentially putting users at risk.

**User Experience Quality**: The unique card-based profile system, date coordination features, and matching algorithms must function seamlessly. Acceptance testing validates that these innovative features are intuitive, reliable, and enhance rather than complicate the user experience.

**Technical Reliability**: As users progress quickly from matching to meeting, the application must perform consistently across different devices, network conditions, and usage scenarios. System crashes or data loss during critical moments (like date setup) could severely impact user trust and safety.

**Business Model Validation**: The acceptance phase tests both the subscription features and advertising integration, ensuring these monetization strategies enhance rather than detract from the core user experience.

**Scalability Preparation**: Testing under various load conditions and user scenarios prepares the application for launch and initial user adoption, identifying performance bottlenecks before they affect real users.

**Regulatory Compliance**: With features like location tracking, identity verification, and personal data management, acceptance testing ensures compliance with privacy regulations (GDPR) and dating app safety standards.

**Market Readiness**: The acceptance phase provides final validation that MEO successfully differentiates itself from competitors while delivering on its core promise of facilitating meaningful real-world connections.

The thoroughness of this acceptance testing phase directly correlates to user safety, satisfaction, and the application's potential for successful market adoption. Given MEO's innovative approach to dating and its emphasis on real-world meetings, this testing phase serves as the crucial bridge between concept and safe, effective implementation.

## 2. Scope

All functionalities of the MEO dating application have been categorized into the following groups for comprehensive testing coverage:

### 2.1 Critical Features

These are essential functionalities without which the application cannot operate properly:

- **User Registration with Phone Number**: Core authentication system using OTP verification
- **Profile Creation with Card System**: Building personalized profiles through various content cards (text, image, audio, music, movie)
- **Matching Algorithm**: Like/dislike system with mutual match creation and appropriate feedback
- **Identity Verification (KYC)**: Internal verification system using ID analysis for safety
- **Date Setup and Management**: Core functionality allowing verified users to propose, accept, and manage real-world meetings
- **Favorite Places Management**: Selection and ranking of preferred date locations (maximum 5 places)

### 2.2 Secondary Functions

These add significant value without being absolutely essential for basic operation:

- **Match Preferences and Filters**: Advanced filtering options (age, height, political stance, lifestyle habits, etc.)
- **Date Editing and Cancellation**: Modification of existing date arrangements
- **User Reporting System**: Safety mechanism for reporting inappropriate behavior
- **Profile Management**: Editing, pausing, and deleting user profiles
- **Notification System**: Push notifications for matches, dates, and reminders

### 2.3 User Interface

Tests focused on user experience, navigation, and accessibility:

- **Navigation Simplicity**: Clear menu structure and intuitive user flow
- **Visual Design**: Modern, cohesive interface with smooth animations
- **Profile Customization**: Visual personalization options and content management
- **Onboarding Flow**: Step-by-step user registration and setup process
- **Card-based Profile Display**: Unique card system for profile content presentation

### 2.4 Compatibility

Ensuring the application functions correctly across different platforms and conditions:

- **Cross-platform Performance**: iOS and Android native compatibility
- **Network Conditions**: Performance under various internet connectivity scenarios (WiFi, 5G, 4G)
- **Device Compatibility**: Functionality across different screen sizes and resolutions
- **System Integration**: Calendar integration, location services, and camera access

---

## 3. Test Plan

### 3.1 Test Scenarios

#### **Scenario 1: Phone Number Registration and OTP Verification**

| **Field**           | **Details**                                                                                                                                                                                                                                                                                                                                        |
| ------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Functionality**   | User registration with phone number and OTP verification                                                                                                                                                                                                                                                                                           |
| **Objective**       | Verify that users can successfully create an account using only their phone number through a secure OTP process                                                                                                                                                                                                                                    |
| **Prerequisites**   | - Valid phone number available<br>- Device with SMS capabilities<br>- Phone number not already registered in system<br>- Internet connectivity                                                                                                                                                                                                     |
| **Steps**           | 1. Launch the MEO application<br>2. Navigate to registration screen<br>3. Select "Sign up with phone number"<br>4. Enter country code and valid phone number<br>5. Accept terms of use (both checkboxes)<br>6. Tap "Send OTP" button<br>7. Receive and enter the 5-digit OTP code<br>8. Complete OTP verification<br>9. Proceed to onboarding flow |
| **Expected Result** | - OTP is sent successfully to provided phone number<br>- User can enter OTP without errors<br>- Account is created upon successful verification<br>- User is redirected to onboarding screen<br>- No duplicate accounts are created                                                                                                                |

---

#### **Scenario 2: Profile Card Creation and Management**

| **Field**           | **Details**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| ------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Functionality**   | Creating and managing profile cards with various content types                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **Objective**       | Validate that users can build comprehensive profiles using the card-based system with different content types                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| **Prerequisites**   | - User is logged in and authenticated<br>- Device has camera and microphone access<br>- Internet connectivity available<br>- Access to device photo library                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| **Steps**           | 1. Navigate to profile editing section<br>2. Tap the "+" button to create new card<br>3. Select card type: Text, Audio, Photo, Music, or Movie<br>4. Choose appropriate prompt for the card<br>5. Add content based on card type:<br>&nbsp;&nbsp;&nbsp;- Text: Type written response<br>&nbsp;&nbsp;&nbsp;- Audio: Record voice message<br>&nbsp;&nbsp;&nbsp;- Photo: Upload or take new photo<br>&nbsp;&nbsp;&nbsp;- Music: Search and select song<br>&nbsp;&nbsp;&nbsp;- Movie: Search and select movie poster<br>6. Save the card<br>7. Verify card appears on profile<br>8. Test card reordering using up/down arrows<br>9. Delete a card using delete button<br>10. Repeat for each card type |
| **Expected Result** | - All card types can be created successfully<br>- Content uploads work for each type<br>- Book covers are rejected as content option<br>- Cards display correctly on profile<br>- Card reordering functions properly<br>- Card deletion works without errors<br>- Maximum card limits are enforced if applicable                                                                                                                                                                                                                                                                                                                                                                                   |

---

#### **Scenario 3: User Matching and Like/Dislike System**

| **Field**           | **Details**                                                                                                                                                                                                                                                                                                                                                                                                                  |
| ------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Functionality**   | Core matching mechanism with swipe functionality                                                                                                                                                                                                                                                                                                                                                                             |
| **Objective**       | Verify the like/dislike system works correctly and creates matches when mutual                                                                                                                                                                                                                                                                                                                                               |
| **Prerequisites**   | - User has completed profile setup<br>- At least 2 other user profiles exist in system<br>- One other profile has already liked the test user<br>- User is on application home screen                                                                                                                                                                                                                                        |
| **Steps**           | 1. Navigate to home screen showing user profiles<br>2. View first profile completely<br>3. Swipe left or tap "X" button (dislike)<br>4. View second profile (one that already liked user)<br>5. Swipe right or tap heart button (like)<br>6. Observe match creation feedback<br>7. Check match appears in matches section<br>8. Test both swipe gestures and button taps<br>9. Verify no match occurs with disliked profiles |
| **Expected Result** | - Like and dislike actions register immediately<br>- Mutual likes create a match with appropriate feedback<br>- Match notification is displayed prominently<br>- Non-mutual likes don't create matches<br>- Both swipe and button interactions work<br>- Liked/disliked users don't reappear in queue                                                                                                                        |

---

#### **Scenario 4: Identity Verification Process (KYC)**

| **Field**           | **Details**                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| ------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Functionality**   | Internal identity verification using ID documents and facial recognition                                                                                                                                                                                                                                                                                                                                                                     |
| **Objective**       | Ensure the KYC process works smoothly and provides appropriate verification status                                                                                                                                                                                                                                                                                                                                                           |
| **Prerequisites**   | - User has completed basic profile creation<br>- Valid government-issued ID available<br>- Device camera functioning<br>- Good lighting conditions                                                                                                                                                                                                                                                                                           |
| **Steps**           | 1. Navigate to identity verification section<br>2. Read verification instructions<br>3. Upload clear photo of government-issued ID<br>4. Position face in camera frame<br>5. Take selfie for facial recognition comparison<br>6. Submit verification documents<br>7. Confirm submission was successful<br>8. Check temporary 'Verified' status appears<br>9. Wait for internal processing completion<br>10. Verify final verification status |
| **Expected Result** | - ID upload process completes without errors<br>- Facial recognition capture works smoothly<br>- Temporary verification status appears immediately<br>- User receives confirmation of submission<br>- Verification is processed internally (not outsourced)<br>- Final verification status updates appropriately<br>- Verified users gain access to date setup features                                                                      |

---

#### **Scenario 5: Date Setup and Coordination**

| **Field**           | **Details**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| ------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Functionality**   | Setting up real-world dates between matched verified users                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **Objective**       | Validate the complete date setup process including location and time coordination                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **Prerequisites**   | - Two verified users have matched<br>- Access to both user accounts/devices<br>- Both users have favorite places configured<br>- Internet connectivity on both devices                                                                                                                                                                                                                                                                                                                                                                                                                  |
| **Steps**           | 1. User A navigates to matches section<br>2. User A selects matched User B<br>3. User A initiates date setup<br>4. User A proposes meeting place from favorites<br>5. User A selects available date and time slots<br>6. User B receives date proposal notification<br>7. User B views proposed date details<br>8. User B suggests alternative location<br>9. User B accepts one of User A's time slots<br>10. User A accepts User B's location suggestion<br>11. Date confirmation is completed<br>12. Test date cancellation by one user<br>13. Test match cancellation functionality |
| **Expected Result** | - Date proposals can be sent and received<br>- Location suggestions work bidirectionally<br>- Time slot selection functions properly<br>- Users can negotiate date details<br>- Final confirmation creates confirmed date<br>- Cancellation options work for both dates and matches<br>- All parties receive appropriate notifications                                                                                                                                                                                                                                                  |

---

#### **Scenario 6: Favorite Places Management**

| **Field**           | **Details**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| ------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Functionality**   | Adding, organizing, and managing preferred date locations                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **Objective**       | Verify users can effectively manage their favorite date venues with proper constraints                                                                                                                                                                                                                                                                                                                                                                                                            |
| **Prerequisites**   | - User is logged in<br>- Location services enabled<br>- Internet connectivity available<br>- Various location search options available                                                                                                                                                                                                                                                                                                                                                            |
| **Steps**           | 1. Navigate to user profile page<br>2. Access favorite places section<br>3. Tap "+" button to add first location<br>4. Use search bar to find and add location<br>5. Add second location using category browse<br>6. Add third location from suggested locations<br>7. Continue adding up to maximum of 5 locations<br>8. Attempt to add 6th location (should be prevented)<br>9. Test reordering locations in priority list<br>10. Remove one location from list<br>11. Add replacement location |
| **Expected Result** | - Can successfully add locations via multiple methods<br>- Search bar, categories, and suggestions all function<br>- Maximum limit of 5 locations is enforced<br>- System prevents adding beyond limit<br>- Location reordering works smoothly<br>- Locations can be removed successfully<br>- All changes are saved persistently                                                                                                                                                                 |

---

#### **Scenario 7: User Reporting System**

| **Field**           | **Details**                                                                                                                                                                                                                                                                                                                                                                                                       |
| ------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Functionality**   | Reporting inappropriate user behavior or safety concerns                                                                                                                                                                                                                                                                                                                                                          |
| **Objective**       | Ensure users can effectively report issues with comprehensive options                                                                                                                                                                                                                                                                                                                                             |
| **Prerequisites**   | - User has active match with another user<br>- User is authenticated and on matches screen<br>- Reporting interface is accessible                                                                                                                                                                                                                                                                                 |
| **Steps**           | 1. Navigate to matches list page<br>2. Select the match to be reported<br>3. Scroll to bottom of match details<br>4. Tap "Report [Username]" button<br>5. Review available reporting categories<br>6. Select appropriate reason for report<br>7. Add detailed description in text field<br>8. Include any relevant additional information<br>9. Submit completed report<br>10. Confirm report submission feedback |
| **Expected Result** | - Report button is easily accessible<br>- Comprehensive reporting options available<br>- Free-text description field allows detail<br>- Report submits successfully<br>- User receives confirmation of submission<br>- User feels supported and safe<br>- Appropriate feedback confirms action taken                                                                                                              |

---

#### **Scenario 8: Advanced Preference Settings and Matching Algorithm**

| **Field**           | **Details**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| ------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Functionality**   | Setting detailed match preferences and validating algorithm effectiveness                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| **Objective**       | Verify the matching algorithm respects user preferences and provides relevant suggestions                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| **Prerequisites**   | - User has detailed completed profile<br>- Multiple diverse user profiles exist in system<br>- User is in preferences/settings section                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| **Steps**           | 1. Navigate to match preferences section<br>2. Set age range preferences (minimum and maximum)<br>3. Configure height and weight preferences<br>4. Set maximum distance radius<br>5. Configure exclusion preferences:<br>&nbsp;&nbsp;&nbsp;- Gender exclusions<br>&nbsp;&nbsp;&nbsp;- Political opinion exclusions<br>&nbsp;&nbsp;&nbsp;- Religious belief exclusions<br>&nbsp;&nbsp;&nbsp;- Lifestyle habit exclusions<br>6. Set sexual orientation preferences<br>7. Save all preference changes<br>8. Navigate to home screen<br>9. Review suggested matches for relevance<br>10. Modify preferences and observe changes |
| **Expected Result** | - All preference categories can be set successfully<br>- Matching algorithm provides relevant suggestions<br>- Preferences significantly impact match results<br>- Location-based matching respects distance limits<br>- Exclusion filters work properly<br>- Users can fine-tune matching criteria<br>- Changes reflect immediately in suggestions<br>- Two-way preference compatibility is enforced                                                                                                                                                                                                                       |

---

#### **Scenario 9: Cross-Platform Performance and Compatibility**

| **Field**           | **Details**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| ------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Functionality**   | Application performance across different devices and network conditions                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| **Objective**       | Validate consistent functionality across platforms and varying technical conditions                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| **Prerequisites**   | - Multiple test devices available (iOS and Android)<br>- Access to different network conditions<br>- Various screen sizes and resolutions<br>- Different OS versions available                                                                                                                                                                                                                                                                                                                                             |
| **Steps**           | 1. Install application on small screen smartphone<br>2. Test all core functionalities on small device<br>3. Install application on tablet/larger device<br>4. Verify responsive design adaptation<br>5. Test on different Android versions<br>6. Test on different iOS versions<br>7. Test functionality on weak WiFi connection<br>8. Test functionality on 4G connection<br>9. Test functionality on 5G connection<br>10. Verify smooth transitions between screens<br>11. Test performance during peak usage simulation |
| **Expected Result** | - Application functions consistently across all devices<br>- No crashes or critical performance issues<br>- Responsive design adapts properly to screen sizes<br>- Functionality remains stable across OS versions<br>- Performance acceptable under various network conditions<br>- Smooth transitions maintained regardless of device<br>- Application remains usable during connectivity changes                                                                                                                        |

---

#### **Scenario 10: Complete User Onboarding Flow**

| **Field**           | **Details**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| ------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Functionality**   | End-to-end new user setup and profile completion                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| **Objective**       | Ensure new users can successfully complete the entire registration and setup process                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| **Prerequisites**   | - Fresh installation of application<br>- Valid phone number for registration<br>- Device camera and location access available<br>- Profile photos ready for upload                                                                                                                                                                                                                                                                                                                                                                                                                 |
| **Steps**           | 1. Complete phone number registration with OTP<br>2. Enter first name and personal information<br>3. Input and verify birth date<br>4. Select gender with optional precision<br>5. Upload clear profile picture<br>6. Set location (GPS or manual entry)<br>7. Fill in physical attributes<br>8. Add professional information<br>9. Configure lifestyle habits<br>10. Set personality traits<br>11. Configure initial match preferences<br>12. Complete profile verification steps<br>13. Create first profile cards<br>14. Set up favorite places<br>15. Review completed profile |
| **Expected Result** | - Complete onboarding process flows smoothly<br>- All required fields can be completed<br>- Optional fields can be skipped appropriately<br>- Location services work properly<br>- Profile picture upload succeeds<br>- Validation prevents invalid data entry<br>- Default preferences apply when fields skipped<br>- User reaches functional home screen<br>- Profile appears complete and attractive<br>- User ready to start matching process                                                                                                                                  |
