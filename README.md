# tsc-event-logger
A reusable and expandable way to do event logging in LabVIEW

Find the VIP here: [![Image](https://www.vipm.io/package/tsc_lib_tsc_event_logger/badge.svg?metric=installs)](https://www.vipm.io/package/tsc_lib_tsc_event_logger/) [![Image](https://www.vipm.io/package/tsc_lib_tsc_event_logger/badge.svg?metric=stars)](https://www.vipm.io/package/tsc_lib_tsc_event_logger/)

Implement event logging in your application.

`Construct` one or more sink types as a way to have multiple places that will track events in the application.

Call `Start Logging` to begin logging in an application and call `Stop Logging` to close down all event logging communication.

`Log Entry` is a malleable VI that provides a way to define inputs for the:
 - Logger - source of the event
 - Level - follows a common definition of event log message level (for sorting/filtering in helper applications)
 - Message - the string that will be appened for the log; messages use a wildcard format defined by { } 's (`{username}` for example) which will be replaced by input arguments
 - Arguments - array of strings that will replace the wildcard markers in the message input

 Additional sinks can be added an removed during the life of the application to show temporary helpers or record specific events.

`Structured Logging` is a software approach that can be learned about in many different formats, but the main tenents are common event levels, timestamps, and formatting of messages so that they can be parsed and filtered by various applications.

### Log Levels
The following are the log levels that are implemented by the framework:
- OFF
- TRACE
- DEBUG
- INFO
- WARN
- ERROR
- FATAL