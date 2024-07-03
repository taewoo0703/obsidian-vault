# ○ handle 함수

```cpp
/** Handle event. Override the handle(..) method in your event handlers to respond to events. */
virtual bool handle(osgGA::Event* event, osg::Object* object, osg::NodeVisitor* nv) { return GUIEventHandler::handle(event, object, nv); }

/** Handle events, return true if handled, false otherwise. */
virtual bool handle(const GUIEventAdapter& ea,GUIActionAdapter& us);
```
