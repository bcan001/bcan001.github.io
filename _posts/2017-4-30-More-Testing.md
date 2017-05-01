---
layout: post
title: More Testing with Rspec
---

Today I had some interesting findings regarding testing and the before(:each) clause. Typically you wouldn't want something to happen before every single one of your tests (such as create a user factory, in this example). Below is an example of how to skip before each actions on certain tests:

before(:each) do |example|
	unless example.metadata[:skip_user_create]
  	@user = FactoryGirl.create(:user, username: Faker::Name.unique.name, email: Faker::Internet.unique.email)
  end
end

describe "GET index" do
  it 'it renders the index template successfully', :skip_user_create do
  	get :index
    expect(response).to be_success
  end

  it "renders the show template" do
    get :show, params: {id: @user.id}
    expect(response).to render_template("show")
  end
end

This example shows the before each clause, as well as one test that skips it and another that uses it. This technique to skip before each clauses will be very handy in my future tests.