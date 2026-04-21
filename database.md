The system uses Supabase as its backend database service. Supabase is
built on PostgreSQL and provides a scalable, secure, and real-time
database solution.

It is used to store all application data, manage user authentication,
and support system workflows.  

# Why Supabase

Supabase was selected because:

- Built on PostgreSQL (reliable and powerful)
- Supports real-time data updates
- Easy integration with frontend and backend
- Cloud-based and scalable

# Database Structure

The database is designed using a relational structure, where data is
stored in tables and linked using relationships.

## Key Data Entities

The system includes several core tables:

### profiles

Stores users information (e.g., full_name, short_name, phone_num)

### announcements

Stores all company announcements (e.g., title, summary, type,
department_id)

### one_to_one

Stores meeting records and notes (e.g., meeting_title, meeting_time,
meeting_bu)

### pbac_settings

Handles approval-based workflows (e.g., user_id, before_json,
after_json)

### Relationships

The database uses relationships to connect data between tables

Examples:

- One user can create many announcements
- One meeting can have multiple tasks
- One user can have multiple approvals

This ensure data consistency and efficient queries.

### abac_policy_metadata

Supabase Authentication is used to manage user login and access.

- Secure login system
- Role-based access integration
- Session management

# Data Flow

1.  User submits data from frontend
2.  Request is sent to backend
3.  Backend communicates with Supabase
4.  Data is stored or retrieved from database
5.  Response is returned to user

# Security

The system uses Supabase security features such as:

- Row Level Security (RLS)
- Role-based data access
- Authentication control

# Benefits

- Centralised data management
- Real-time updates
- Secure and scalable
- Easy integration with system modules
