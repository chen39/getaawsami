AWS CLI

aws ec2 describe-images \ 
--owners 'amazon' \
--filters 'Name=description,Values=Amazon Linux AMI*' \
--query 'sort_by(Images, &CreationDate)[-1].[ImageId]' \
--output 'text'
