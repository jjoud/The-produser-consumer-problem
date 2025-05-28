class Producer implements Runnable {
    Queue q;

    Producer(Queue q) {
        this.q = q;
        new Thread(this, "Producer").start();
    }

    public void run() {
        for (int i = 0; i < 30; i++) {
            q.put(i);
            try {
                Thread.sleep(500); // Delay for 0.5 seconds
            } catch (InterruptedException e) {
                System.err.println("InterruptedException caught: " + e.getMessage());
            }
        }
    }
}
