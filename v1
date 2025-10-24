class Patient:
    def __init__(self, name, surname, age):
        self.name = name
        self.surname = surname
        if age >= 0:
            self.age = age
        else:
            self.age = 0
        self._next = None

    def set_next(self, p):
        self._next = p

    def get_next(self):
        return self._next

    def get_name(self):
        return self.name.strip()

    def get_surname(self):
        return self.surname.strip()

    def get_age(self):
        return self.age

    def get_count(self, count=0):
        count += 1
        if self.get_next() is None:
            return count
        else:
            return self.get_next().get_count(count)


    def get_last(self):
        if self._next is None:
            return self
        else:
            return self.get_next().get_last()



class WaitingRoom:
    def __init__(self, size=10):
        self._patients = []
        self.size = size
        self.first = None
        #self.last = None


    def get_last(self):
        return first.get_last()


    def add(self, p: Patient):
        if self.first is None:
            self.first = p

        else:
            if self.get_count() + 1 > self.size:
                    raise (OverflowError)
            self.get_last().set_next(p)


    def remove(self) -> Patient:
        if self.first is None:
            return None
        else:
            tempP = self.first
            self.first = self.first.get_next()
            return tempP

    def get_count(self):
        if self.first is None:
            return 0
        else:
            return self.first.get_count()
