# impove sentence

## question

I have ecommerce web site which and I have used devise gem and it well installed into my app and I have been trying to make it be protected where before do anything he\she must login but till now every user can go anywhere he or do in my system which is bad news is there where I should protect my system

here is my controller

```
class UsersController < ApplicationController
  before_action :set_user, only: [:show, :edit, :update, :destroy]

    def index
      if params[:term]
        @users = User.where('first_name LIKE ? or last_name LIKE ?', "%#{params[:term]}%", "%#{params[:term]}%").page(params[:page])
        else
          @users = User.all.page(params[:page])
        end
      end

    def show
    end

    def destroy
        @user.destroy
        redirect_to users_url, notice: 'User was successfully destroyed.'
    end

    private
    def set_user
      @user = User.find(params[:id])
    end
  end
```
