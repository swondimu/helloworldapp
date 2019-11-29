# helloworldapp

import UIKit

class ViewController: UIViewController {
    
    @IBOutlet weak var textField: UITextField!
    @IBOutlet weak var textHello: UILabel!
    
    var backgroundColor: UIColor!
    override func viewDidLoad() {
        super.viewDidLoad()
        // Do any additional setup after loading the view.
        backgroundColor = view.backgroundColor
    }

    @IBAction func didTapButton(_ sender: Any) {
        textHello.textColor = UIColor.orange
    }
    @IBAction func didTapViewButton(_ sender: Any) {
        view.backgroundColor = UIColor.purple
        
    }
    @IBAction func didTapTextButton(_ sender: Any) {
        //textHello.text = "Goodbye!"
        textHello.text = textField.text
        view.endEditing(true)
    
    }
   
    @IBAction func didTapResetButton(_ sender: Any) {
        textHello.text = "Hello"
        textHello.textColor = UIColor.black
        view.backgroundColor = backgroundColor
    }
    
}

