Temporary states can be saved in Session variables for workflow control.

Session.setDefault('isFormModal', false);
User is on a form page {Session.set('isFormModal', true) } -> selects contacts button -> views contacts -> selects a contact -> 
   if Session.get('isFormModal') 
      { return to form page } 
      else
      { return edit contact page}
        
