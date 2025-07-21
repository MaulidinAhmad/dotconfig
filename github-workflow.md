#/.ssh/.gitconfig<br />
[includeIf "gitdir:~/projects/work/**"]<br />
    &nbsp;&nbsp;path = .gitconfig-work<br />
[includeIf "gitdir:~/projects/personal/**"]<br />
   &nbsp;&nbsp; path = .gitconfig-personal<br />

#.ssh/.gitconfig-work<br />
#work config<br />
[user]<br />
 &nbsp;&nbsp; name = Ahmad Maulidin Al Furqon<br />
&nbsp;&nbsp;  email  = ahmadmaulidin@test.com<br />


# .ssh/config
Host github.com-work<br />
#AddKeysToAgent yes<br />
#UseKeychain yes<br />
&nbsp;&nbsp;  HostName github.com<br />
&nbsp;&nbsp;  User git<br />
&nbsp;&nbsp; IdentityFile ~/.ssh/id_ed25519<br />
&nbsp;&nbsp;  IdentitiesOnly yes<br />
<br />
#rahul-personal account<br />
Host github.com-personal<br />
#AddKeysToAgent yes<br />
#UseKeychain yes<br />
&nbsp;&nbsp;  HostName github.com<br />
&nbsp;&nbsp;  User git<br />
&nbsp;&nbsp;  IdentityFile ~/.ssh/personal-github<br />
 &nbsp;&nbsp; IdentitiesOnly yes<br />

#windows<br />
Start-Service ssh-agent<br />
ssh-add ~/.ssh/work-github<br />


#how to use
git clone ssh@ahmad.github.com-work/test
