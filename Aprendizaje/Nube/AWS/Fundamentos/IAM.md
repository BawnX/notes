#Cloud #AWS #Fundamentos

[[Daily/2024-04-15.md|2024-04-15]]

```table-of-contents
title: 
style: nestedList # TOC style (nestedList|inlineFirstLevel)
minLevel: 0 # Include headings from the specified level
maxLevel: 0 # Include headings up to the specified level
includeLinks: true # Make headings clickable
debugInConsole: false # Print debug info in Obsidian console
```
**Identity and Access Management (IAM)** es un servicio gratuito que nos ayuda a administrar los accesos a los servicios y recursos de tu cuenta en AWS. A su vez, puedes crear usuarios, grupos y establecer permisos de acceso a los recursos mediante el uso de políticas.

# **Usuarios y grupos de usuarios de IAM**

Los usuarios y grupos de usuarios son de los principales componentes de IAM. Al crear tu cuenta de AWS te proporcionan un **usuario Root** que tiene acceso a todos los recursos,

Este usuario puede generar otros perfiles y cada uno con un acceso único a distintos recursos de AWS. Además, Root también puede configurar grupos de usuarios, donde cada miembro tiene y puede compartir permisos de acceso.

# **Ejemplos de políticas de IAM**

El acceso a recursos se otorga mediante políticas. Este es un ejemplo de una política que otorga acceso de administrador.

```
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Effect": "Allow",
            "Action": "*",
            "Resource": "*"
        }
    ]
}
```

También está este ejemplo de políticas de acceso a un bucket de S3 (almacenamiento)

```
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Effect": "Allow",
            "Action": [
                "s3:ListBucket"
            ],
            "Resource": "arn:aws:53 ::: bucket-name"
        },
        {
            "Effect": "Allow",
            "Action": [
                "s3: GetObject",
                "s3: PutObject",
            ],
            "Resource": "arn:aws:53 ::: bucket-name /*"
        }
    ]
}
```

# **IAM Roles**

Además de todas estas funciones, **IAM de AWS** permite asumir roles y otorgar permisos a otras tecnologías. Por ejemplo, podemos conceder a una máquina virtual el acceso a una base de datos mediante un rol de IAM.
