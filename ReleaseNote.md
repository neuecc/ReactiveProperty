# Release note

## v2.2.8

### Changes

- Changed implements interface to ReactiveProeprty and ReadOnlyReactiveProperty. Issue #11.

## v2.2.7

### Changes

- Changed internal implementation in IFilteredReadOnlyObservableCollection.

## v2.2.6

### Add

- Add AddRangeOnScheduler method to ReactiveCollection class.

## v2.2.5

### Update

- Update System.Windows.Interactivity assembly reference.

## v2.2.4

### BugFix

- Fixed bug, FilteredReadOnlyObservableCollection index management were broken when collection item removed.
- Fixed bug, FilteredReadOnlyObservableCollection index management were broken when collection item replaced.

## v2.2.3

### BugFix

- Fixed bug, converter called when ReadOnlyReactiveCollection remove method called.

## v2.2.2

### BugFix

- Fixed bug, have Problem in initialization at FilteredReadOnlyObservableCollection index.

## v2.2.1

### Bug fix

- Fixed bug, call several times Subscribe method in the constructor of ReadOnlyReactiveProperty.

## v2.2

### Breaking changes

- Remove ObserveElementReactiveProperty extension method.

### Add

- Add ObserveElementObservableProperty extension method.

## v2.1.8

### Add

- Added FilteredReadOnlyObservableCollection<T> class at Helpers namespace. It is real time filtered collection.

## v2.1.7

### Bug fix

- Fixed bug. ReadOnlyReactiveProperty<T> did not use the value to be issued as the initial value from BehaviorSubject<T> when made BehaviorSubject<T> to the source.

## v2.1.6

- Implemented ObserveElementReactiveProperty extension method, to observe ReactiveProeprty which ObservableCollection and ReadOnlyObservableCollection elements have changing.
- Implemented ObserveElementPropertyChanged extension method, to observe PropertyChanged event which ObservableCollection and ReadOnlyObservableCollection elements have.
- Implemented ReadOnlyReactiveProperty<T> class. ToReadOnlyReactiveProperty extension method creates its instance from IObservable<T>.  

### Breaking change

- Changed accesibility of ObserveElementProperty method to 'internal' from 'public'. 

## v2.1.5

### Add

- Add create ReadOnlyReactiveCollection method from IEnumerable.

## v2.1.4

- Not released.

## v2.1.3

### Breaking change

- ObserveElementProperty returns instance which has value changed property.

## v2.1.2

### Add

- Implemented ObserveElementProperty extension method, to observe property changes of the ObservableCollection elements and ReadOnlyObservableCollection elements.
- Added ObserveXxxChanged extension methods for INotifyCollectionChanged.

### Change

- Remove class constranit from ToReadOnlyObservableCollection extension method.

## v2.1.1

### Change

- Changed exception which is occured when UIDispatcherScheduler is initialized under SynchronizationContext.Current is null.

## v2.1.0

### Add

- Add ToReadOnlyReactiveCollection extension method to ReadOnlyObservableCollection.
	- readOnlyObservableCollectionInstance.ToReadOnlyReactiveCollection(x => CreateViewModel(x))

### Change

- Dispose method is called in collection when ReadOnlyReactiveCollection called dispose method.

## v2.0.1

### Change

- Implements INotifyPropertyChanged to BooleanNotifier.

## v2.0.0

### Breaking change

- Change namespace Codeplex.Reactive to Reactive.Bindings
- Rename ReactiveProperty#ObserveHasError to ReactiveProperty#ObserveHasErrors.

### Obsolate

- EventToReactive obsolated. Please use EventToReactiveProperty or EventToReactiveCommand.

### Change

- ReadOnlyReactiveProperty call Dispose method when item removed.
- Implements INotifyPropertyChanged to CountNotifier..

### Add

- Add features for Xamarin.Android
    - SetBinding extension method added to View class.
    - SetCommand  extension method added to IObservable<T>.
