desc 'Generate a new KEY USAGE: rake "gen_key[domainname]"'
task :gen_key, :domainname do |task, args|
  filename = "#{args[:domainname]}.key"

  sh "openssl genrsa -des3 -out #{filename} 2048"
end

desc 'Generate a new CSR USAGE: rake "gen_csr[domainname]"'
task :gen_csr, :domainname do |task, args|
  csr_filename = "#{args[:domainname]}.csr"
  key_filename = "#{args[:domainname]}.key"
  
  sh "openssl req -new -sha256 -key #{key_filename} -out #{csr_filename} -subj '/C=JP/ST=Tokyo/L=Bunkyo-ku/O=feedforce, Inc./OU=Development Group/CN=#{args[:domainname]}'"
  puts sh "openssl req -noout -text -in #{csr_filename}"
end
