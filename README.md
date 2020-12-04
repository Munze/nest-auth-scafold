# nest-auth-scafold

initial nestjs with passport and jwt authorization scaffolding.
Added GraphQL AuthGuard and @CurrentUser decorator.
- GqlAuthGuard overrides the getRequest() method
- To get the current authenticated user in your graphql resolver, you can define a @CurrentUser() decorator:
- like: 
  @Query(returns => User)
  @UseGuards(GqlAuthGuard)
  whoAmI(@CurrentUser() user: User) {
  return this.usersService.findById(user.id);
  }
  
No db just mockup list od names
Based on NestJS documentation
