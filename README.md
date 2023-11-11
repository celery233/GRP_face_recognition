# Face Detection &Recognition

## Decision
|Problem|Solutions|
|  ---- | ----    |
|The understanding of pytest is not particularly deep. Unable to automate test procedures|Learn pytest on related websites, and write scripts to complete automated testing.|
|The comparison accuracy of photos after face recognition is low.|Establish training to make the recognized photos easier to compare. Optimized code|
|Cannot use the camera to test the code.|Look for clear pictures on the Internet to compare.|
|Distinguish between real people and images|A blink test to ask users to do a sequence of motions. (several ideas instead of coding)|
|The obtained image is low resolution|Use super-resolution technology to improve photo quality. (FSRCNN)|
|The initialize function needs to check for empty folders but gitlab cannot exist empty folders|Change the function to let him detect jpg and png files in the folder|
|Accessories such as glasses on the person will affect the contrast accuracy|Use glasses detection to check and ask to take off the glasses that have a big impact|
|Expression affects the accuracy of comparation|Smile detection, requires the person to be detected to have a serious face|



## Testing
| Test ID |Test Description | Inputs | Expected Outcome | Test Outcome | Result |
| ----    |      -------    |  ----  |      ----        |    ----      | ----   |
|1.1     |Test same people|"testa.jpg" "testa"  | 1 |1 | pass |
|1.2     |Test same people|"testb.jpg" "testb"  | 1 |1 | pass |
|1.3     |Test similar but different people|"testc.jpg" "testc"  | 0 |0 | pass |
|1.4     |Test similar but different people|"testd.jpg" "testd"  | 0 |0 | pass |
|2.1     |Test glass|"testglass"          |N <= 8|3| pass |
|2.2     |Test no glass|"testnoglass"        |0  |0 | pass |
|3.1     |Test smile|"smile"              |N <= 1| 0 | pass|
|3.2     |Test no smile|"nosmile"              |N <= 1 |0| pass |

