# SSH

In order to connect to your EC2 instance, you can use SSH.
Remember to have your `.pem` file and run this command in your termin:

```shell
ssh -i your_pem_file.pem <ec2-username>@<your_public_ipv4>
```

If you get a warning saying "UNPROTECTED PRIVATE KEY FILE", that's because you need to:

```shell
chmod 0400 your_pem_file.pem
```

This allows the owner of the file permissions to read it.
