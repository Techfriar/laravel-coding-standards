[<<Back](../README.md)

# Developer Testing Examples

## Unit Testing

```php
public function testUserCanChangePassword()
{
    $user = User::factory()->create();
    $user->changePassword('newpassword');
    $this->assertTrue(Hash::check('newpassword', $user->password));
}
```

## Unit Testing
```php
public function testUserCanLogin()
{
    $user = User::factory()->create();

    $response = $this->post('/login', [
        'email' => $user->email,
        'password' => 'password',
    ]);

    $response->assertRedirect('/dashboard');
    $this->assertAuthenticatedAs($user);
}
```