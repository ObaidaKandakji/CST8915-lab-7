# CST8915-lab-7

## youtube link
https://youtu.be/DfqLxZMmRtU

## Questions

**Is RabbitMQ stateless or stateful?**  
- This implementaion of RabbitMQ is stateless

**Implications of running RabbitMQ without persistent storage**  
- Data is not saved anywhere longterm.  
- After a restart queues and messages are lost.

**What happens when the RabbitMQ pod is deleted or restarted?**  
- Kubernetes starts a new pod with an empty data directory.  
- Any queues/messages created earlier are lost.  
- Only default settings from env vars remain.

**Potential solutions**  
- Use a managed messaging service instead of running RabbitMQ locally.

**Does Azure Service Bus solve these issues?**  
- Yes  since its a managed service Azure handles the high availability and storage requirements and we don't need to maintain RabbitMQ ourselves.  