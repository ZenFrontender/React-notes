
When we implement lazy loading onto a component or components, and when we navigate to a component which is lazy loaded. We encounter an error of Rendering getting suspended and the component is not loaded.
we encounter that error when the user tried to navigate to that component, a n/w call gets made to fetch the JS file required for that component, it will cause a delay whether it is of few mS 9only but when we tried to load that component the required JS file was not there. Hence we encounters an error of rendering getting suspended.


But we don't encounter this error of rendering getting suspended anymore . If we dont use suspense, we don't see anything on the page until that component is fetched and rendered but no more error. But if we use lazy loading we can show a message meanwhile that component is getting fetched

%% when using lazy loading cause  React Router is handling Suspense for lazy-loaded routes behind the scenes.  
If you use lazy loading outside of route elements, you must wrap those components in `<Suspense>`.  
For route elements, React Router v6+ does it for you. %%


For using <suspense> we wrap the component inside suspense and suspense has an attribute fallback where we can define what we want to display when the component is still getting loaded

eg:

{
path: '/grocery',
component: (
<suspense fallback={<h1>Grocery component loading ...</h1>} >
	<Grocery />
<suspense />
)
}