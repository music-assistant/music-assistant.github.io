# MA get_library Action

This action allows you to retrieve the full details of the items from the library

![image](../assets/screenshots/service-call/get_library.png)

As can be seen there are a large number of filter options available.

The returned JSON is extensive. The [returned data can be used in templates](https://www.home-assistant.io/docs/scripts/perform-actions#use-templates-to-handle-response-data).

## Example

In this example a queue of 10 random tracks is created.

```
script:
  create_random_queue:
    mode: single
    sequence:
      - service: mass.get_library
        data:
          limit: 10
          media_type: track
          order_by: random
        response_variable: random_tracks
      - repeat:
          count: "{{ random_tracks | length + 1}}"
          sequence:
            - action: mass.play_media
              data:
                media_id: "{{ random_tracks.tracks[repeat.index - 1].uri }}"
                media_type: track
                enqueue: add
              target:
                entity_id: media_player.ma_kitchen_speaker
```