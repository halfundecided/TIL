### Tags attribute 
- `sender.tag` : 같은 IBAction안에 있는 components들을 구별. 

### Sound effects 
- `import AVFoundation`

### Playing sound recipe
````swift
import UIKit
import AVFoundation

class ViewController: UIViewController, AVAudioPlayerDelegate{

    var audioPlayer: AVAudioPlayer!

    override func viewDidLoad() {
        super.viewDidLoad()
    }
    @IBAction func notePressed(_ sender: UIButton) {
        
        let soundURL = Bundle.main.url(forResource: "note1", withExtension: "wav")
        do {
            audioPlayer = try AVAudioPlayer(contentsOf: soundURL!)
        }
        catch {
            print(error)
        }   
        audioPlayer.play()
    }
}
````

### Scope 
 






### ref
- Apple Developer Forum: https://forums.developer.apple.com/
- Apple API Reference: https://developer.apple.com/reference/
- Apple Guides and Sample Code: https://developer.apple.com/library/content/navigation/
