**Customer Theory**

 

**Financial Risk System**

​       A global investment bank based in India, New York and Singapore trades (buys and sells) financial products with other banks (“*counterparties*"). When share prices on the stock markets move up or down, the bank either makes money or loses it. At the end of the working day, the bank needs to gain a view of how much risk of losing money they are exposed to, by running some calculations on the data held about their trades. The bank has an existing Trade Data System (TDS) and Reference Data System (RDS) but needs a new Risk System.

 

**Trade Data System (TDS)**

The Trade Data System maintains a store of all trades made by the bank. It is already configured to generate a file-based XML export on a network share of trade data at the close of business (5pm) in NewYork. The export includes the following information for every trade made by the bank: 

• Trade ID, Date, Current trade value in US dollars, Counterparty ID

**Reference Data System (RDS)**

The Reference Data System maintains all of the reference data needed by the bank. This includes

Information about counterparties; each of which represents an individual, a bank, etc. A file-based XML

Export is also available on a network share and includes basic information about each counterparty. A new organization-wide reference data system is due for completion in the next 3 months, with the current system eventually being decommissioned

 

The high-level requirements for the new Risk System are as follows.

 Import trade data from the Trade Data System and Import counterparty data from the Reference Data System. Join the two sets of data together, enriching the trade data with information about the Counterparty, for each counterparty, calculate the risk that the bank is exposed to. Generate a report that can be imported into Microsoft Excel containing the risk figures for all counterparties known by the bank.

 Distribute the report to the business users before the start of the next trading day (9am) in

Singapore. Provide a way for a subset of the business users to configure and maintain the external parameters used by the risk calculations.

 

Cross Cutting Concerns with Financial Risk System

a.    Risk reports must be generated before 9am the following business day in Singapore.

b.    The system must be able to cope with trade volumes for the next 5 years.

c.    The Trade Data System export includes approximately 5000 trades now and it is anticipated  that there will be slow but steady growth of 10 additional trades per day

d.    The Reference Data System export includes approximately 20,000 counterparties and growth will be negligible

e.    There are 40-50 business users around the world that need access to the report.

f.     Risk reports should be available to users 24x7, but a small amount of downtime (less than 30 minutes per day) can be tolerated

g.    Manual failover is sufficient, provided that the availability targets can be met.

h.    This system must follow bank policy that states system access is restricted to authenticated and authorized users only

i.     Reports must only be distributed to authorized users

j.     Only a subset of the authorized users are permitted to modify the parameters used in the risk calculations

k.    Although desirable, there are no single sign-on requirements (e.g. integration with Active Directory, LDAP, etc)

l.     All access to the system and reports will be within the confines of the bank’s global network.

m.   The following events must be recorded in the system audit logs

​                                i.   Report generation

​                               ii.   Modification of risk calculation parameters

​                              iii.   It must be possible to understand the input data that was used in calculating risk.

n.    The system should take appropriate steps to recover from an error if possible, but all errors should be logged

o.    Errors preventing a counterparty risk calculation being completed should be logged and the process should continue

p.    All user interfaces will be presented in English only

q.    All reports will be presented in English only

r.    All trading values and risk figures will be presented in US dollars only

s.    A Simple Message trap should be sent to the bank’s Central Monitoring Service in the following circumstances

​                                i.   When there is a fatal error with a system component

​                               ii.   When reports have not been generated before 9am Singapore time

t.    Input files used in the risk calculation process must be retained for 1 year

u.    Interfaces with existing data systems should conform to and use existing data formats.

 
