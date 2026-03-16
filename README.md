## Prisma and Express Setup ( Follow Prisma Original Doc if Need)
    - Node  22.0
## Intialize node project 
    - npm init -y 
## Install Typescript and Setup 
    - npm install typescript 
    - npx tsc --init
    > Copy Paste Entire tsconfig.json code 

##  Add Script in package.json
    - copy the script from package.json 
#  Install dependencies 
### Runtime Dependencies
    - npm install @prisma/adapter-pg @prisma/client dotenv express pg
### Dev Dependencies
    - npm install -D prisma typescript @types/express @types/node

## Run Prisma Generate command
    - npx prisma init
    (you will get schema.prisma file just keep the same as i keep)
    Before Generate Command Update dot env file as i wrote wrote same liek that 
    DATABASE_URL=postgresql://postgres:mysecret@localhost:5432/userdb

    - npx prisma generate
    - npx prisma migrate dev

    if any migration already exists in the DB then you have to run this 

    - npx prisma migrate reset

    then re run this
    - npx prisma migrate dev

    promt message

### Create src folder inside that index.ts 
    - Copy paste the code 

## Run Application 
    - npm run build
    - npm run start 

## To chekc the DB record run this command 
    - npx prisma studio

## If you change DB name then run again this command 
    - npm prisma migrate dev

## Using Docker Check
    - docker exec -it 4835e6b2acb7 psql -U postgres -d employeeDB
    - \dt;
    - SELECT * FROM "User";
