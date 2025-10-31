# slide-and-catch
class Lenny(simpleGE.Sprite):
    def __init__(self, scene):
        super().__init__(scene)
        self.setImage("dog.png")
        self.setSize(50, 50)
        self.position =(320, 400)
    
class Game(simpleGE.Scene):
    def __init__(self):
        super().__init__()
        self.setImage("farm.png")
        self.lenny = Lenny(self)
        
        self.sprites = [self.lenny]
def main():
    game = Game()
    game.start()
    
if __name__ == "__main__":
    main()
