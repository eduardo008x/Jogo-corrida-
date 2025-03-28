import javax.swing.*;
import java.awt.*;
import java.awt.event.ActionEvent;
import java.awt.event.ActionListener;
import java.awt.event.KeyEvent;
import java.awt.event.KeyListener;
import java.util.ArrayList;
import java.util.Iterator;
import java.util.Random;

public class CorridaSimples extends JPanel implements ActionListener, KeyListener {
    private int larguraJanela = 400;
    private int alturaJanela = 600;
    private int larguraCarro = 50;
    private int alturaCarro = 80;
    private int posicaoCarroX = 175;
    private int posicaoCarroY = 500;
    private int velocidadeCarro = 20;
    private int velocidadeObstaculo = 5;
    private Timer timer;
    private ArrayList<Rectangle> obstaculos;
    private Random random;
    private boolean jogoRodando = true;

    public CorridaSimples() {
        setPreferredSize(new Dimension(larguraJanela, alturaJanela));
        setBackground(Color.DARK_GRAY);
        setFocusable(true);
        addKeyListener(this);

        obstaculos = new ArrayList<>();
        random = new Random();

        timer = new Timer(30, this);
        timer.start();
    }

    public void paintComponent(Graphics g) {
        super.paintComponent(g);

        if (jogoRodando) {
            // Desenha o carro
            g.setColor(Color.RED);
            g.fillRect(posicaoCarroX, posicaoCarroY, larguraCarro, alturaCarro);

            // Desenha os obstáculos
            g.setColor(Color.WHITE);
            for (Rectangle obstaculo : obstaculos) {
                g.fillRect(obstaculo.x, obstaculo.y, obstaculo.width, obstaculo.height);
