# Dependency-Injection
HAHA, I've been using dependency injections soooo many times without knowing what they are called.
The simplest example is below.

protocol Driving {
    func startDriving()
    func isDriving() -> Bool
    func stopDriving()
}

class BMV: Driving {
    func startDriving() {
        print("BMV is being started.")
    }
    
    func isDriving() -> Bool {
        print("BMV is being driven.")
        return true
    }
    
    func stopDriving() {
        print("BMV is being stopped")
    } 
    
}

class Honda: Driving {
    func startDriving() {
        print("Honda is being started.")
    }
    
    func isDriving() -> Bool {
        print("Honda is being driving.")
        return true
    }
    
    func stopDriving() {
        print("Honda is being driven.")
    }
    
}

class SelectedCar {
    
    var car: Driving
    
    init(car: Driving) {
        self.car = car
    }
    
}
