import pygame
from random import randint

pygame.init()

app = pygame.display.set_mode((1440, 800), pygame.RESIZABLE)
width = int(app.get_width())
haight = int(app.get_height())
pygame.display.set_caption('Ritual Ping Pong 🕹️✨')

font = pygame.font.SysFont('pixel', 100)
p1wins = font.render('Player 1 wins! ⚡ Ritual Power', True, (0, 0, 255))
p1wins_rect = p1wins.get_rect().width
p2wins = font.render('Player 2 wins! ⚡ Ritual Strong', True, (0, 0, 255))
p2wins_rect = p2wins.get_rect().width

font2 = pygame.font.SysFont('pixel', 50)
numChoose = font2.render('Choose players for Ritual Ping Pong: (1 = vs AI, 2 = vs Player)', True, (0, 0, 255))
numChoose_rect = numChoose.get_rect().width

ritual_text = font2.render('🏓 Welcome to Ritual Ping Pong!', True, (255, 0, 0))
ritual_text_rect = ritual_text.get_rect().width


class Area(pygame.sprite.Sprite):
    def __init__(self, x_pos, y_pos, player_width, player_haight, speed=0, AI=False, color=(0,0,0)):
        super().__init__()
        self.rect = pygame.Rect(x_pos, y_pos, player_width, player_haight)
        self.speed = speed
        self.fill_color = color
        self.AI = AI

    def reset(self):
        pygame.draw.rect(app, self.fill_color, self.rect)


class Player(Area):
    def updateP1(self):
        keys = pygame.key.get_pressed()
        if keys[pygame.K_UP] and self.rect.y > 5:
            self.rect.y -= self.speed
        if keys[pygame.K_DOWN] and self.rect.y < 2*haight/3-5:
            self.rect.y += self.speed

    def updateP2(self):
        if self.AI:
            if not self.rect.y+width/6 == ball.rect.y:
                if ball.rect.y < self.rect.y+width/12:
                    self.rect.y -= self.speed
                else:
                    self.rect.y += self.speed
        else:
            keys = pygame.key.get_pressed()
            if keys[pygame.K_w] and self.rect.y > 5:
                self.rect.y -= self.speed
            if keys[pygame.K_s] and self.rect.y < 2 * haight / 3 - 5:
                self.rect.y += self.speed


class Ball(pygame.sprite.Sprite):
    def __init__(self, x, y, radius, speed=0, color=(255,255,255)):
        self.radius = radius
        self.color = color
        self.speed = speed
        self.rect = pygame.Rect(x-radius, y-radius, 2*radius, 2*radius)

    def draw(self):
        pygame.draw.circle(app, self.color, self.rect.center, self.radius)

    def move(self):
        self.rect.x += self.speed[0]
        self.rect.y += self.speed[1]
        if self.rect.top <= 0 or self.rect.bottom >= haight:
            if self.speed[1] > 0:
                self.speed[1] += 1
            else:
                self.speed[1] -= 1
            self.speed[1] *= -1

    def collision(self, object):
        if self.rect.colliderect(object.rect):
            if self.speed[0] > 0:
                self.speed[0] += 1
            else:
                self.speed[0] -= 1
            self.speed[0] *= -1


player1 = Player(143*width/144-width/72, haight/3, width/72, haight/3, 6, False, (0,0,255))
player2 = Player(width/144, haight/3, width/72, haight/3, 6, False, (0,0,255))

nx = randint(-1, 1)
while nx == 0:
    nx = randint(-1, 1)
ny = randint(-1, 1)
while ny == 0:
    ny = randint(-1, 1)

ball = Ball(width/2-10, haight/2-10, 20, [nx*2, ny])


run = True
start = False
gameapp = True
clock = pygame.time.Clock()
FPS = 60
timeToChoose = True
close = 0

while run:
    width = int(app.get_width())
    haight = int(app.get_height())
    if width < 180:
        width = 180
    if haight < 90:
        haight = 90

    app.fill((0, 255, 0))  

    if not timeToChoose:
        for e in pygame.event.get():
            if e.type == pygame.QUIT:
                run = False

        if not start:
            if gameapp:
                app.blit(ritual_text, (width/2 - ritual_text_rect/2, 50))
                ball.draw()
                ball.collision(player1)
                ball.collision(player2)
                ball.move()
                player1.updateP1()
                player1.reset()
                player2.updateP2()
                player2.reset()

        if ball.rect.x > width:
            app.blit(p2wins, (width/2-p2wins_rect/2, haight/2))
            start = True
            close += 1
        if ball.rect.x < 0:
            app.blit(p1wins, (width/2-p1wins_rect/2, haight/2))
            start = True
            close += 1

        if close > 200:
            run = False
    else:
        app.blit(numChoose, (width/2-numChoose_rect/2, haight/2))
        for e in pygame.event.get():
            if e.type == pygame.QUIT:
                run = False
            elif e.type == pygame.KEYDOWN:
                if e.key == pygame.K_1:
                    player2.AI = True
                    timeToChoose = False
                elif e.key == pygame.K_2:
                    player2.AI = False
                    timeToChoose = False

    pygame.display.update()
    clock.tick(FPS)
