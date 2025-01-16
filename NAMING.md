# Naming Conventions

### Basic GuideLines:
- Classes/ReactComponents: CamelCase starting with capital letter.
- Functions/.... : CamelCase starting with small letter.
- Classes/Objects: Noun (Manager/Runner)
- Functions: Verbs (manage/run)

Good read. [naming cheatsheet](https://github.com/kettanaito/naming-cheatsheet/blob/main/README.md)

What Causes Bad Variable Names?
Most problems with naming variables stem from
- A desire to keep variable names short
- A direct translation of formulas into code

## Arrays:
- users
- userList
- userGroup
- userCollection

## Maps:
- userIdToUser
- userIdToUserMap
- usersByUserId

## Array of Arrays:
- userLists
- userGroups
- userCollections

## Boolean:
- isVisible
- shouldShow
- hasEdited
- is****Enabled   ( isFontanaApprovalsEnabled / isOpexEnabled )
- shouldShow****   (shouldShowFooter/showShowTabs)
- doesUserHave****   (doesUserHaveRights/doesUserHavePermissions)
- is*****In****     (isEmailInWhiteListedEmails/isUserInApproverList)
- does***ListContain****  (doesAdminUserEmailsContainEmail)
- isEmail****   (isUserWhiteListed)
