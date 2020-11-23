# Answer

as you can see you installed devise but you didn't add protection into your route while devise is waiting for you to tell how is allowed to access you controllers.

inorder to tell devise who is allowed to access controller you will need to add this line of code

```
class UsersController < ApplicationController
  before_action :set_user, only: [:show, :edit, :update, :destroy]
 before_action :authenticate_user!

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

## before_action :authenticate_user!

this line of code it will force ever use to login before he\she do anything to your ecommerce

## before_action :set_user, only: [:show, :edit, :update, :destroy]

this line of code it will help you grant user access to your ecommerce like `show, :edit, :update, :destroy`
