# Simple notes on YII2
Example creating notes page

## Create requests on your db (or use dump - notes.sql): ##
```
CREATE TABLE `notes` (
  `id` int(11) NOT NULL,
  `date` date NOT NULL,
  `uid` int(11) NOT NULL,
  `theme` varchar(200) COLLATE utf8_bin NOT NULL,
  `text` text COLLATE utf8_bin NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8 COLLATE=utf8_bin;


INSERT INTO `notes` (`id`, `date`, `uid`, `theme`, `text`) VALUES
(1, '2019-01-01', 1, 'New theme', 'Test note for new theme');


ALTER TABLE `notes`
  ADD PRIMARY KEY (`id`);

ALTER TABLE `notes`
  MODIFY `id` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=15;
COMMIT;
```

## Paste view in your app (notes.php)

## Create model in your app
```PHP
<?php

namespace app\models;

use yii\db\ActiveRecord;
use yii\base\Model;

class Notes extends ActiveRecord
{	
}
?>
```
