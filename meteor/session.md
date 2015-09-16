Temporary states can be saved in Session variables for workflow control.

Session.setDefault('isFormModal', false);
User is on a form page {Session.set('isFormModal', true) } -> selects contacts button -> views contacts -> selects a contact -> 
   if Session.get('isFormModal') 
      { return to form page } 
      else
      { return edit contact page}
        



Alternatively, consider using React + Meteor.  It's helpful to review Flux Architecture for ideas and reference.  Flux is more for large scale development.

Standard react package by MDG is react without the :
