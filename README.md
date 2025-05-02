
# 📄 JMeter Test Plan: Assignment 2

## 🗂️ Overview
This JMeter test plan is designed to simulate and validate a set of HTTP requests to a `/Books` API. It performs actions such as POST, PUT, DELETE, and GET operations.

---

## 🧪 Thread Group Configuration

| Name                 | Number of Threads | Ramp-Up Time | Loop Count |
|----------------------|-------------------|--------------|------------|
| Unnamed Thread Group | N/A               | N/A          | 1          |

---

## 🌐 HTTP Request Details

| Sampler Name | Method | Protocol | Domain | Path              |
|--------------|--------|----------|--------|-------------------|
| N/A          | POST   | N/A      | N/A    | `/Books`          |
| N/A          | PUT    | N/A      | N/A    | `/Books/13`       |
| N/A          | POST   | N/A      | N/A    | `/books/authToken`|
| N/A          | POST   | N/A      | N/A    | `/Books`          |
| N/A          | DELETE | N/A      | N/A    | `/Books/34`       |
| N/A          | GET    | N/A      | N/A    | `/Books`          |

---

## 📌 Notes

- Most HTTP sampler names are not defined (marked as `N/A`).
- The thread group is minimally configured and may require manual setting of user count, ramp-up, and domain values.
- These endpoints suggest operations typical for a book management API.
- Consider using `HTTP Request Defaults` to define the domain and protocol globally for all samplers.
