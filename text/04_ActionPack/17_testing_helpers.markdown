## Testare gli helper con semplicità

Una delle cose più noiose nelle prime versioni di Rails era testare gli **helpers**. Creare un test che coprisse al 100% un **helper** era molto complesso.

In Rails 2.1 è diventato tutto più semplice grazie alla classe **ActionView::TestCase**. Ad esempio:

	module PeopleHelper
	  def title(text)
	    content_tag(:h1, text)
	  end

	  def homepage_path
	    people_path
	  end
	end

Osservate come possiamo fare lo stesso in Rails 2.1:

	class PeopleHelperTest < ActionView::TestCase
	  def setup
	    ActionController::Routing::Routes.draw do |map|
	      map.people 'people', :controller => 'people', :action => 'index'
	      map.connect ':controller/:action/:id'
	    end
	  end

	  def test_title
	    assert_equal "<h1>Ruby on Rails</h1>", title("Ruby on Rails")
	  end

	  def test_homepage_path
	    assert_equal "/people", homepage_path
	  end
	end
