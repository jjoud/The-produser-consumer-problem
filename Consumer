class Consumer implements Runnable {
    Queue q;

    Consumer(Queue q) {
        this.q = q;
        new Thread(this, "Consumer").start();
    }

    public void run() {
        for (int i = 0; i < 30; i++) {
            q.get();
            try {
                Thread.sleep(1000); // Delay for 1 second
            } catch (InterruptedException e) {
                System.err.println("InterruptedException caught: " + e.getMessage());
            }
        }
    }
}
