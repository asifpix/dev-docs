1. Get username by user ID using JUser Class. (Method 1)
```
$userId = 42; // Replace with the actual user ID
$user = JFactory::getUser($userId);
echo $user->name; // Outputs the user's name
```
2. Get username by user ID using database query. (Method 2)
```
$userId = 42; // Replace with the actual user ID
$db = JFactory::getDbo();
$query = $db->getQuery(true)
    ->select($db->quoteName('name'))
    ->from($db->quoteName('#__users'))
    ->where($db->quoteName('id') . ' = ' . (int) $userId);
$db->setQuery($query);
$authorName = $db->loadResult();
echo $authorName; // Outputs the user's name
```