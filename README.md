import pygame, simpleGE, random

class Lenny(simpleGE.Sprite):
    def __init__(self, scene):
        super().__init__(scene)
        self.setImage("dog.png")
        self.setSize(50, 50)
        self.position =(320, 400)
        self.moveSpeed = 5
    def process(self):
        if self.isKeyPressed(pygame.K_LEFT):
            self.x-=self.moveSpeed
        if self.isKeyPressed(pygame.K_RIGHT):
            self.x += self.moveSpeed
    
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
