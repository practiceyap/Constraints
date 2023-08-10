# Constraints
<pre>
```swift
 // Провести проверку по корректности лейблов (profileLogin, profileDescription) - trailing нужен ли для них или нет.Ё
        NSLayoutConstraint.activate([
            profileImageView.topAnchor.constraint(equalTo: safeAreaLayoutGuide.topAnchor, constant: 32),
            profileImageView.leadingAnchor.constraint(equalTo: leadingAnchor, constant: 16),
            profileImageView.heightAnchor.constraint(equalToConstant: 70),
            profileImageView.widthAnchor.constraint(equalToConstant: 70),
            
            profileName.topAnchor.constraint(equalTo: profileImageView.bottomAnchor, constant: 8),
            profileName.leadingAnchor.constraint(equalTo: profileImageView.leadingAnchor),
            trailingAnchor.constraint(equalTo: profileName.trailingAnchor, constant: 16), // Чтобы был отступ справа если будет к примеру такое имя: Константин Константинопольский
            
            profileLogin.topAnchor.constraint(equalTo: profileName.bottomAnchor, constant: 8),
            profileLogin.leadingAnchor.constraint(equalTo: profileName.leadingAnchor),
            // Для profileLogin скорей всего тоже нужен trailing т.к отступ должен быть справа тоже на 16.
            
            profileDescription.topAnchor.constraint(equalTo: profileLogin.bottomAnchor, constant: 8),
            profileDescription.leadingAnchor.constraint(equalTo: profileName.leadingAnchor),
            // Для profileDescription скорей всего тоже нужен trailing т.к отступ должен быть справа тоже на 16.
            
//            logOutButton.trailingAnchor.constraint(equalTo: trailingAnchor, constant: -20),
            trailingAnchor.constraint(equalTo: logOutButton.trailingAnchor, constant: 20),
            logOutButton.centerYAnchor.constraint(equalTo: profileImageView.centerYAnchor)
        ])
```
</pre>
