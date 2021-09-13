class User():
    def __init__(self,
                 username,
                 password,
                 idNumber,
                 isAdmin,
                 pastReservations
    ):
        self.username = username
        self.password = password
        self.idNumber = idNumber
        self.isAdmin = isAdmin
        self.pastReservations = pastReservations

    def is_authenticated(self):
        return True
    
    def is_active(self):
        return True

    def is_anonymous(self):
        return False

    def get_id(self):
        return str(self.idNumber)

    def get_pastReservations(self):
        return self.pastReservations
    def set_pastReservations(self, a):
        self.pastReservations = a

    def hasBooked2Hours(self, date):
        hours = 0
        if date not in self.pastReservations:
            return False
        for court in self.pastReservations[date]:
            hours += len(self.pastReservations[date][court])
        if(hours>=2):
            return True
        else:
            return False
