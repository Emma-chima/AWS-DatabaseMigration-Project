# 📦 My First AWS DMS Project – Just Learning Stuff

Hey 👋

This is just me documenting my very first attempt at using **AWS Database Migration Service (DMS)**. I’m still learning my way around cloud stuff, and this little project was a practical way to get a feel for how DMS works.

## 💡 What I Did

I created a simple MySQL database called `employees`, with just one table called `staff`. It’s not anything fancy—just a few rows of dummy data like names and job positions.

The goal? **Migrate it from MySQL to PostgreSQL** using AWS DMS.

That’s literally it.

## 🛠️ Steps I Took

1. **Created the MySQL database and table** manually through the CLI.
2. **Created a replication instance** on AWS.
3. **Set up source and target endpoints** — source was MySQL, target was PostgreSQL.
4. Ran a **premigration assessment** (failed the first time lol).
5. Granted the necessary **permissions to the DMS user** on MySQL.
6. Created the **migration task** and ran it.
7. Finally, I **checked the target PostgreSQL DB** and boom, the `staff` table was there.

## 😩 Some Challenges I Faced

- **The premigration assessment failed** at first. Took me a while to realize I hadn’t granted enough privileges to the `admin` user in MySQL.
- Also forgot to set the **database name in the endpoint config**, so nothing was migrating until I fixed that.
- Had to run some AWS CLI commands a couple of times to figure things out.
- It wasn’t super obvious at first how the DMS roles and permissions worked, so I had to do some trial and error.

## ✅ What I Learned

- How to set up and run a DMS migration task (finally 😅).
- That **permissions are super important**—without the right GRANTs, nothing works.
- How to use the **AWS CLI** to check the status of migration tasks and troubleshoot.
- Also learned how to clean up my resources properly so I don't get billed for things I’m no longer using.
